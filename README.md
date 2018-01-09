# Show Specific Dictionaries for CCExtractor

This repository is a collection of show specific dictionaries that CCExtractor can take as an argument to explicitly specify the [letter case](https://en.wikipedia.org/wiki/Letter_case) for the words in the dictionary appearing in extracted subtitles. CCExtractor also has a generic 11,000 words dictionary located in [`/Dictionary`](https://github.com/CCExtractor/ccextractor/tree/master/Dictionary) directory.
## Usage

Use `--capfile /path/to/file/` or `-caf /path/to/file/` parameter of CCExtractor to pass the dictionary. This parameter adds the contents of 'file' to the list of words that must be capitalized. 

For example, if file is a plain text file that contains

```
	Tony
	Alan
```

**Whenever those words are found they will be written exactly as they appear in the file.**

So from

```
             YOU BETTER RESPECT
             THIS ROBE, ALAN
```

you get 

```
             YOU BETTER RESPECT
             THIS ROBE, Alan
```

This is generally used in conjunction with `--sentencecap` or `-sc` which tell ccextractor to follow the typical capitalization rules, such as capitalize months, days of week, etc.

Thus, using them together gives 

```
             You better respect
             this robe, Alan.
```

## Instructions to Create Dictionaries

- Lines starting with `#` are considered comments and discarded.

- Use one line per word. 

- Naming convention is `dict _showname.txt`.

- The words in dictionary must be in lexicographical order (dictionary order).

- The words in dictionary that are found will be written exactly as they appear in the file, so this is needed to be kept in mind.

## Support

By far the best way to get support is by opening an issue at our [issue tracker](https://github.com/CCExtractor/show_specific_dictionaries/issues). 

When you create a new issue, please fill in the needed details in the provided template. That makes it easier for us to help you more efficiently.

If you have a question or a problem you can also [contact us by email or chat with the team in Slack](https://www.ccextractor.org/doku.php?id=public:general:support). 

If you want to contribute to CCExtractor but can't submit some code patches or issues or video samples, you can also [donate to us](https://www.ccextractor.org/public:general:http:sourceforge.net_donate_index.php?group_id=190832). 

## Contributing

You can contribute to the project by reporting issues, forking it, modifying the code and making a pull request to the repository. We have some rules, outlined in the [contributor's guide](.github/CONTRIBUTING.md).

## News & Other Information

For more information visit the CCExtractor website: [https://www.ccextractor.org](https://www.ccextractor.org)

## License

GNU General Public License version 2.0 (GPL-2.0)