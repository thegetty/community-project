---
title: How to Contribute to This Publication
subtitle: 
layout: essay
order: 20
---

Before getting started, make sure you have the following installed: 

- [GitHub Desktop](https://desktop.github.com/download/)
- [Node.js](https://nodejs.org/en/download) 
- [Quire CLI](https://quire.getty.edu/docs-v1/install-uninstall/) 
- [Visual Studio Code](https://code.visualstudio.com/) or a comparable free text editor  

***

## Getting Set Up to Make Your Contribubtion

This section walks you through cloning the project from GitHub so you can add your pet, and then opening the project in Visual Studio Code so you can make your contribution. 

### GitHub 

1. Navigate to this publication repository on Github: https://github.com/thegetty/community-project
2. Clone the repo by clicking the green "Code" button on upper-right side of the page and chose "Open with GitHub Desktop"
3. Naviate to "Current Branch" at the top of the page and select "New Branch"
4. Create a new branch off of "main" and title your branch following this pattern: `[name]-addition` for example `erin-addition`

### Terminal 

1. Open your command-line shell 
2. Type `cd community-project` and hit enter 
3. Type `npm install` and hit enter
4. Type `quire preview` and hit enter
5. Open your browser, navigate to <http://localhost:8080/>, and preview the project 

### Visual Studio Code 

1. Open Visual Studio Code 
2. Go to File>Open Folder
3. Navigate to your home directory and open the `community-project/content/` folder 
4. Go to File>Auto Save to turn on autosave otherwise your changes might not appear. 


***

## Add Your Pet 

Follow these steps to actually add your pet to this publication. This includes making changes to the `_asset/images/` folder, adding an entry to the `figures.yaml` file, create a `.md` file for your pet, add a shortcode to pull in your pet's picture, add your content. 

### Add Your Image to the `_assets` folder

1. Navigate to the `content/_assets/images/pet-pics/` folder and drag-and-drop an image of your pet into this folder. The file name should be your pet's name in all lowercase letters followed by `.jpg` or `.png` depending on the file type (for example, `delilah.jpg`). Please note, the extension must be all lowercase. 

### Create a Figure Entry in `figures.yaml`

1. Navigate to the `content/_data/figures.yaml` file and fill out one of the blank entries with your pet's information. Make sure all your content is surrounded by quotes. 
2. Replace one the `id` of one of the blank entries (for example, replace `pet-XX` with your pet's name). The `id` must start with a letter and include no spaces as demonstrated by the other examples in this file.
3. For `src` add `pet-pics/` followed by your file name created in the section above (for example, `pet-pics/delilah.jpg`).
4. For `caption` add whatever you would like. 
5. For `alt` add a short visual description of your pet. This is used by screen readers for visually impaired readers. 

### Add Content to a `.md` File 

1. Navigate to the  `content/critters/` folder and choose one of the blank `XX-pet.md` files. 
2. Right click on the file name and rename it after your pet (for example `delilah.md`).
3. Update the Page YAML:  
- For `title` replace "Your Pet's Name Here" with your pet's name.  
- Keep `layout` and `order` the same. 
- Repalce `Your First Name` and `Your Last Name` with your own name. 
- Delete `toc: false` and `menu: false`. If you do not delete this, your entry will be hidden. 

### Use A Shortcode to Add Your Pet's Pic

1. Cut and paste the following text at the top of your entry, under the page YAML section: 
`{% figure 'id' %}`
2. Replace `id` with the `id` you added in the `figures.yaml` entry (for example, `delilah`). The `id` is *not* the same as the `src` and should *not* include an extension. 

### Add your Markdown Content 

1. Add a short bit of text to tell the rest of the community about why your pet or chosen critter is awesome! 
2. Feel free to style the text using [Markdown](https://quire.getty.edu/docs-v1/fundamentals/).  


 ### Preview Your Project to Make Sure Everything Worked

 1. If you already have the preview running, press Control+C to stop the preview
 2. Run the command `quire preview`
 3. If everything word you will see your pet added as a new entry in catalogue section.
 4. If you receive error messages, it's most likely an issue with the YAML. Run your `figures.yaml` entry and Page YAML into a YAML validator like Code Beautify: https://codebeautify.org/yaml-validator. 
