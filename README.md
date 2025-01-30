# Webscrapping_zeolites

As part of an **introduction and initiation research internship** at the Laboratory of Separation and Reaction Processes - Laboratory of Catalysis and Materials (LSRE-LCM), the goal of the proposed work was to **create a database that could be used in future techniques of Machine Learning**, based on a zeolite site of the IZA (International Zeolite Association) that contained the properties of interest.

To achieve this, it was necessary to use ``Python`` techniques, resorting mainly to ``Pandas`` library (essentially used for data manipulation and analysis), ``NumPy`` (when manipulating data through vectors), as well as ``BeautifulSoup`` and ``requests``. These last two libraries allowed me to find the information of interest within the HTML (programming language used to create the web pages), functioning as a tool to access and read the code. Further the work, there was also the necessity to resort to the ``openpyxl`` library, mainly for formatting (reading and writing) files in Excel, for advanced data processing.

To carry out the work of taking the properties of interest, it was necessary research and elaboration of a search methodology within the site and the development of a Python routine in Google Collaboratory.

Taking into account what was proposed, it was obtained a database that contains the following information:
- the Zeolite Types;
- the Unit Cell Shape;
- each Space Group;
- the lengths a, b and c;
- the amplitudes α, β and γ;
- the Framework Density;
- their Ring Sizes;
- the Channels dimensions;
- Maximum diameter of a sphere, that can be included;
- Maximum diameter of a sphere, that can diffuse along;
- the Accessible Volume;
- the Natural Tiling;
- the Composite Building Units;
- each Chemical Formula and a column for additional information, all that with the corresponding units.
It was also created a database containing the list of T-atoms for each zeolite.

For the searching part of the process, I mainly resorted to two methods: using the the ``Pandas`` library or the ``BeautifulSoup`` one.
The first method uses the code ``pd.read_html`` and searches for all the HTML code of the page defined with the ``<table>`` tag (HTML tables), transforming the information taken from these tables into a ``Pandas DataFrame``.
The second method turned out to be a bit more complex, however essential when the information of interest was not found within a ``<table>`` tag. Recurring to the code ``requests.get`` from ``requests`` library, it was obtained the entire HTML code of the page through an HTTP request to the web server. After that, it was possible to use the ``BeautifulSoup`` library to find any part of the code, defined with any tag and even associated with specific attributes. As an example, we have the case of the “Space Group” property, whose information is defined with the ``<div>`` tag.

Figure 1

Figure 2
In the first image (figure 1), it is possible to see a part of the database that was created, in Excel format, with some of the properties of interest.
In the second image (figure 2), it is presented one of the tables referring to the list of T-atoms of a zeolite, also in Excel format. Visible in the lower part of the image, there is also a list of pages, each one corresponding to a different type of zeolite.
In short, this internship allowed me to learn both the Python programming language, as well as HTML, while also learning to scrape data from multiple pages of the IZA website and concatenate them all into a single DataFrame.
