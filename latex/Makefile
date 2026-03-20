# LaTeX build system for CSE 211 project documents
#
# Usage:
#   make base             Build base.pdf
#   make proj-01          Build PROJ-01.pdf
#   make projects         Build all 25 project PDFs
#   make all              Build everything
#   make clean            Remove build artifacts
#
# Version is derived automatically from git tag + current date.
# Override manually: make all VERSION=v3.0 DATE=2026-09-15

LATEX    := pdflatex
OUTDIR   := build

# ── Auto-detect version from git tag ──
# On exact tag:     v1.0.0
# Between tags:     v1.0.0+2 (2 commits ahead)
# No tags:          dev
GIT_TAG   := $(shell git describe --tags --abbrev=0 2>/dev/null || echo "")
GIT_AHEAD := $(shell git rev-list $(GIT_TAG)..HEAD --count 2>/dev/null || echo "0")
VERSION   ?= $(if $(GIT_TAG),$(if $(filter 0,$(GIT_AHEAD)),$(GIT_TAG),$(GIT_TAG)+$(GIT_AHEAD)),dev)
DATE      ?= $(shell date +%Y-%m-%d)

# Inject version/date as LaTeX \def before \documentclass picks up \providecommand
DEFS     := "\def\thedocversion{$(VERSION)}\def\thedocdate{$(DATE)}\input{main}"
FLAGS    := -interaction=nonstopmode -halt-on-error -file-line-error

PROJ_IDS := $(shell printf 'PROJ-%02d\n' $$(seq 1 25))

# ── Base document ──
.PHONY: base
base: $(OUTDIR)/base.pdf

$(OUTDIR)/base.pdf: base/main.tex base/metadata.tex base/sections/*.tex base/appendices/*.tex shared/*.tex
	@mkdir -p $(OUTDIR)
	@echo "Building base.pdf [$(VERSION) / $(DATE)]"
	cd base && $(LATEX) $(FLAGS) -output-directory=../$(OUTDIR) -jobname=base $(DEFS)
	cd base && $(LATEX) $(FLAGS) -output-directory=../$(OUTDIR) -jobname=base $(DEFS)

# ── Individual project (e.g., make proj-01) ──
.PHONY: proj-%
proj-%: $(OUTDIR)/PROJ-%.pdf
	@true

$(OUTDIR)/PROJ-%.pdf: projects/PROJ-%/main.tex projects/PROJ-%/metadata.tex projects/PROJ-%/content.tex shared/*.tex
	@mkdir -p $(OUTDIR)
	@echo "Building PROJ-$*.pdf [$(VERSION) / $(DATE)]"
	cd projects/PROJ-$* && $(LATEX) $(FLAGS) -output-directory=../../$(OUTDIR) -jobname=PROJ-$* $(DEFS)
	cd projects/PROJ-$* && $(LATEX) $(FLAGS) -output-directory=../../$(OUTDIR) -jobname=PROJ-$* $(DEFS)

# ── All projects ──
.PHONY: projects
projects: $(foreach id,$(PROJ_IDS),$(OUTDIR)/$(id).pdf)

# ── Everything ──
.PHONY: all
all: base projects

# ── Clean ──
.PHONY: clean
clean:
	rm -rf $(OUTDIR)

.DEFAULT_GOAL := all
