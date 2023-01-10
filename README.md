VAHC Homepage
=============

The homepage of Workshop on Visual Analytics in Healthcare (VAHC).

Install and Quick Start
-----------------------

The VAHC homepage is built based on [Pelican](), a Python-powered static site generator. You can install Pelican via several different methods. The simplest is via Pip and specify using markdown:

```bash
python -m pip install "pelican[markdown]"
```

Then, you can clone the repo and go to the root folder of the cloned repo:

```bash
pelican -r -l
```

The default local dev site will be served at `http://localhost:8000/`.
You can now open web browser and check the website for development.


Settings
--------

Due to the special needs of hosting a conference website, some settings in the `pelicanconf.py` have been customized to support conference hosting workflow.

1. `DEFAULT_YEAR`. It's obvious that you need to set this variable to the conference year accordingly.
2. `PAST_EVENTS`. This will be used for generating the footer links to past events.
3. `*_SAVE_AS`. Some features are not used by a simple conference website, such as author page, tag page, archive page, category page, etc. So, they are all disabled and removed from output list.

Workflow
--------

The content structure of each year is very similar (or just the same) to previous year. So you can create a new website for the coming year as follows:

1. Duplicate a latest year folder in `content` and rename to target year. For example, copy the folder `2023`, paste and rename it to `2024` for the 2024.
2. Update the `Category` value in **ALL** `.md` files in the newly created folder. For example, update `Category: 2024` in the `2024\index.md`, `2024\call-for-papers.md`, etc. As this category value will be used to generate the URL and folder, please ensure you updated **ALL** category information correctly. Otherwise the generated HTML files of other year may be affected.
3. Update the contents of each article in the new folder.