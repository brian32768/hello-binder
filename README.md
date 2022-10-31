# hello-binder
Test of mybinder.org

Binder is a cloud-based service that lets you load up and run customized Python notebooks.

The goal of this test was to see if I could get it to load and run a project that uses the Esri ArcGIS Python API.

Step one is to create a repository. The repo needs to have a conda environment and a notebook.
I created the environment and then exported it:

```bash
conda create --name=binder -c esri arcgis
conda activate binder
conda export --from-history -f environment.yml
git add index.ipynb environment.yml
git commit -m initial -a
git push
```

Step two is to go to MyBinder.org and tell it the location of the repository.

Binder will then build a Docker container and load up whatever you specified in environment.yml,
and set up a Notebook environment for you.

Then you can run the notebook, modify it etc.. all in the browser window.
You can launch the project in this repository using this URL: https://mybinder.org/v2/gh/brian32768/hello-binder/main?labpath=index.ipynb

## Resources

https://mybinder.org Front page of the Binder

https://gesis.org Leibniz Institute of Social Sciences

https://arcgis.com Esri

