# Minimal makefile for Sphinx documentation
#

# You can set these variables from the command line.
SPHINXOPTS    =
SPHINXBUILD   = sphinx-build
SPHINXPROJ    = sphinx-test
SOURCEDIR     = source
BUILDDIR      = .


# Put it first so that "make" without argument is like "make help".
help:
	@$(SPHINXBUILD) -M help "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

.PHONY: help Makefile

# Catch-all target: route all unknown targets to Sphinx using the new
# "make mode" option.  $(O) is meant as a shortcut for $(SPHINXOPTS).
%: Makefile
	@$(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "$(BUILDDIR)" $(SPHINXOPTS) $(O)

clean:
	@echo "Removing everything under 'html/ doctrees/ docs'.."
	# @rm -r $(BUILDDIR)/html/ $(BUILDDIR)/doctrees $(BUILDDIR)/docs/
	ls | grep -E -v '^Makefile|^source' | xargs rm -r

update: ## clean -> htmlの後に、htmlフォルダ
	echo "update docs"
	make clean html
	cp -r html/* .