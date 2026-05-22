# Beauty Search

A C++ Trie-based search engine for makeup product discovery and multi-prefix product matching.

## Overview

Beauty Search allows users to search through a simulated Sephora-style makeup product dataset using a multi-prefix search powered by a Trie data structure.

The program works like an autocomplete-style keyword search system. It returns full product records that match all given prefix terms, making it possible to search by product type, skin type, brand-related terms, or category keywords.

## Project Goal

The goal of this project was to apply the Trie data structure to build a fast prefix-based search engine for a makeup product database. The Trie supports efficient lookup on partial search terms and returns complete product records from a structured dataset.

The dataset is organized by:

- Brand
- Skin type
- Category
- Product name

## Key Features

- Trie-based prefix searching
- Multi-prefix search support
- Fast autocomplete-style lookup
- Structured makeup product dataset
- Efficient string matching in C++
- Interactive terminal-based search interface

## Trie Data Structure Design

The Trie is implemented using a nested character node system. Each node contains:

- A map of child nodes pointing to the next character
- A set of full product lines stored at the end of each word

This design allows the program to:

- Insert individual words from each product line
- Retrieve all full product lines containing words that start with a given prefix
- Support multi-prefix queries by intersecting results from each prefix

Key Trie operations:

```cpp
insert(string word, string line)