# Wyam Statuspage

**Just for fun.** Uses [Wyam][2] to reproduce [pyup.io's statuspage][1] project.

For information on how to configure a GitHub repository issues for use with **statuspage**, please see the README on their project page: <https://github.com/pyupio/statuspage>

Here is what this Wyam script does...

  * Reads in a Razor script (as a Wyam document)
  * Get the GitHub user and repository name
  * Uses the [GitHub module][4] to get all the...
    * Labels 
    * Recent issues (past 90 days)
  * Process the Razor script, runs the logic...
    * *Loosely adapted from **statuspage**'s [`statuspage.py`][5] source-code*
  * Outputs HTML and assets

...and **_ta-dah!_** You have a statically-generated status page!

**Next step...**

Wire this up to an AppVeyor CI build, using GitHub's webhook for "Issues" events, for [Continuous Integration][6].

---

### Credits

HTML and CSS assets are taken from the [@pyupio/statuspage][1] repository.

Wyam logos are taken from [wyam.io][3] website repository.


### Just for fun!

This was a fun project, developed in a couple of hours, with no intention of serious use.

Have a question? Feel free to [raise an issue](https://github.com/leekelleher/wyam-statuspage/issues).

Licensed under the [MIT License](LICENSE.md).


[1]: https://github.com/pyupio/statuspage
[2]: http://wyam.io
[3]: https://github.com/Wyamio/Wyam.Web
[4]: http://wyam.io/modules/github
[5]: https://github.com/pyupio/statuspage/blob/master/statuspage.py
[6]: http://wyam.io/knowledgebase/continuous-integration