# Submitting with Github.

#### Video Instructions: [Private Public Github Repo Setup](https://youtu.be/kOZxQyfllYY)

1. Create a completely empty private repo. This should be free, but please tell us if it is not. [Add us as collaborators by going into settings -> collaborators](https://stackoverflow.com/questions/7920320/adding-a-collaborator-to-my-free-github-account). Our github tags are: @ouwen @kevinczhou @roarke, @mariachacko, @a-poorva


2. Clone the class repo. (If you already cloned skip this step). This repo is refered to as the `origin` and we start on the `master` branch.
```bash
git clone https://github.com/Ouwen/BME-590-Machine-Learning-in-Imaging
cd ./BME-590-Machine-Learning-in-Imaging
```

3. Add your private repo as a remote. You can get the url from step 1.
```bash
git remote add private <your-url>
```

4. To pull `origin` updates run the following command:
```bash
git pull origin master
```

5. To push your local changes to your private repo run the following command:
```bash
git push private master
```

6. To make more local changes, go ahead and update the `homework_0.ipyn` to introduce yourself. Then run the following commands.
```bash
git add ./path/to/updated/file #adds the path to be tracked for changes
git commit -m "Your message on what this commit is about"
git push private master
```

6. To submit homework, go to the homework folder you are submitting, copy the URL, and paste it into the homework google form. This will submit the master branch to us. (If you want to submit an older commit or a different branch, just link the URL of the folder to us.)


7. Sometimes when you pull from `origin` there will be a merge conflict. This means I changed a file, and you changed a file. Anything in the session folder, go with my changes. Anything in the homework folder, keep your change. You should be able to run the following in the case of a merge conflict:
```bash
git checkout --theirs ./session
git checkout --ours ./homework
```
