## What could possibly go wrong?

#### I ran the starter code but got a ModuleNotFound error.

You'll be installing two new modules to your PythonData environment for this homework.

- Make sure you check the documentation for each for the correct installation command.
- Make sure you have your PythonData environment activated before you install them.
- Make sure you install them before you launch jupyter notebook, or close jupyter notebook and stop the service in terminal before you attempt to re-run your code after installing.

#### I did all that, and even checked `conda list` and/or `pip freeze` to make sure they were installed. No dice. Still ModuleNotFound.

Yeah, sometimes jupyter notebook just goes sideways on us. It's imperfect, but we love it anyway. Here's some things to try:

- Create a new test environment with just the modules that are causing errors and launch jupyter notebook from within that environment. To refresh your memory, you can use `conda create --name test python=3.6` to create a bare bones environment. Activate it, then install the problematic modules. Launch jupyter notebook, create a new ipynb file, and run a code block where you attempt to import only the problem module. If it still says ModuleNotFound...
- Close down all open notebooks and terminal windows running jupyter. From the command line, with your PythonData environment open, run `conda install -c anaconda ipykernel` then `python -m ipykernel install --user --name=PythonData`. Launch jupyter notebook again. Open the problematic file and in the kernel menu go to bottom where it says Change Kernel and select PythonData from the list. Now you will be able to specifically select your PythonData environment from within a jupyter notebook. You'll also see PythonData in the list under New on the folder outline page, so you can start new ipynb files specifically using your PythonData environment. The down side to this is that with every new ipynb document you open from class activities, you'll probably have to change the kernel to PythonData every time before you run it. (source: https://medium.com/@nrk25693/how-to-add-your-conda-environment-to-your-jupyter-notebook-in-just-4-steps-abeab8b8d084)

#### Ok, all my modules import successfully now, but when I run `gmap.figure()` to output a map nothing shows up in the output.

The jupyter-gmaps module can be picky about exactly how it is installed. The documentation gives you several options, but we've seen more folks have better luck with the pip version of the installation that goes like this:
```
$ jupyter nbextension enable --py --sys-prefix widgetsnbextension

$ pip install gmaps

$ jupyter nbextension enable --py --sys-prefix gmaps
```
If you've already installed it, that's ok. Run `conda remove gmaps`, then try that three-step process above to reinstall. You'll have to completely close any open notebooks and close down the terminal running jupyter with `ctrl-C` and wait until all the messages finish printing and you get your prompt again before attempting to relaunch it.

#### Great. Now I get an error that says something is wrong with my google api key and I should check the browser console.

Ah! We got this. Remember those google APIs we enabled in our project in the google cloud console for class? The jupyter-gmaps module requires the Google Maps Javascript API to be enabled for the API key you're using. Head on over to the cloud console, make sure you're in the right project for the API key you are using, and enable the Google Maps Javascript API. Don't forget to adjust the restrictions on your API key to include the new API. And remember restrictions settings changes may take five minutes to take effect.

#### Something still isn't working.

That's what we're here for. Send us a slack message or ask about it in office hours. We'll get you sorted. You really are doing great!
