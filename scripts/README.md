# How to install tools missing from a toolkit in a new instance

Warning: This procedure assumes the installation of new tools follows the same process as usegalaxy.org : [Requesting a new tool or updating a tool](https://github.com/galaxyproject/usegalaxy-tools?tab=readme-ov-file#requesting-a-new-tool-or-updating-a-tool)

Download the toolkit file. E.g. : [VGP toolkit file](https://github.com/galaxyproject/usegalaxy-playbook/blob/main/env/main/files/galaxy/config/panel_views/vgp.yml)
Clone the repository containing the tools of the target instance

In an empty repository (so as not to erase existing files), run the command : 
```bash
python parse_tools_to_produce_yml_files.py --tk $toolkit_file --yml-folder $install_repository
```

It will generate a set of files named  section.yaml.

Look at the folder containing the installed tools in the target instance. If a section already exist, merge the two files with the same name.
Move the section.yaml files to the target instance repository and folllow the procedure for tool installation : [Requesting a new tool or updating a tool](https://github.com/galaxyproject/usegalaxy-tools?tab=readme-ov-file#requesting-a-new-tool-or-updating-a-tool)
