## New Project Workflow

1. Install cookiecutter
   1. <code> pip3 install cookiecutter </code>
   2. <code> brew install cookiecutter </code>
   3. <code> sudo apt-get install cookiecutter </code>
   4. <code> conda install -c conda-forge cookiecutter </code>
2. Run <code> cookiecutter https://github.com/firatoncu/ds-project-template </code>
   1. Follow the instructions and make necessary changes for requested project parameters.
   2. BE SURE THAT generated project slug is the same for gitlab project slug
3. Initialize a local Git Repository
4. Configure User for Git Repository
   1. <code> git config user.email <"user.email"> </code>
   2. <code> git config user.name <"user.name"> </code>
5. Create an Empty Repository 
   1. Create a Blank project, but be sure that projects slug you provided to be the same with the one used in cookiecutter.
6. Add remote repository to your local git repository
   1. <code> git remote add origin <your_project_url> </code>
7. Commit the generated cookiecutter template and push to the remote branch.