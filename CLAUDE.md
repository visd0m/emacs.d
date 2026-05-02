# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This repository contains my personal Emacs configuration files. The setup uses org-babel to manage configuration in a single `config.org` file, which is then loaded by `init.el`. The configuration is managed using `straight.el` for package management and `use-package` for package configuration.

## Key Files

- `config.org` - Main configuration file written in org-mode with code blocks
- `init.el` - Loads the org configuration file
- `default.el` - Lockfile tracking package versions managed by straight.el

## Development Workflow

To work with this Emacs configuration:

1. **Understand the structure**: The main configuration is in `config.org` which uses org-babel to execute Emacs Lisp code blocks
2. **Loading configuration**: The `init.el` file loads the org file using `org-babel-load-file`
3. **Package management**: Uses `straight.el` with `use-package` for package management
4. **Testing**: Start Emacs with `emacs -Q` to test changes, or use `M-x org-babel-load-file` to reload the config

## Common Tasks

- **Adding new packages**: Add to `config.org` using `use-package` blocks
- **Modifying existing configuration**: Edit the appropriate code blocks in `config.org`
- **Updating packages**: Run `M-x straight-pull-all` or `M-x straight-update-packages`
- **Reloading configuration**: Use `M-x org-babel-load-file` or restart Emacs

## Architecture

The configuration follows a modular approach:
- **Misc**: Basic settings, package management, and utilities
- **UI**: User interface configuration including themes, modeline, and visual elements
- **Completion**: Completion frameworks (vertico, consult, marginalia, embark)
- **Coding**: Language support, LSP integration, and development tools
- **Editing & Movement**: Navigation and editing enhancements
- **AI**: AI-related tools and integrations
- **Custom functions**: Personal utility functions

## Key Features

- Uses `straight.el` for package management
- LSP integration for multiple languages (Rust, Elixir, Elm, Python, etc.)
- Modern completion frameworks (vertico, consult, embark)
- Custom keybindings and utility functions
- Integration with various development tools and services
- Support for multiple programming languages and environments