Requests: HTTP for Mensen
=========================


.. image:: https://travis-ci.org/kennethreitz/requests.png?branch=master
        :target: https://travis-ci.org/kennethreitz/requests

Requests (Verzoeken) is een Python bibliotheek voor echte mensen, met een Apache2 software-licentie

De meeste bestaande Python modules die HTTP verzoeken versturen zijn extreem verboos en lastig. De meeste HTTP mogelijkheden die je nodig hebt zitten ook in Python's urllib2, maar deze api is volledig disfunctioneel. Het vereist bijzonder veel moeite om urllib2 aan de praat te krijgen (zelfs het overschrijven van methodes) voor de simpelste dingen.

Dit is niet hoe het hoort. Zeker niet in Python.

.. code-block:: pycon

    >>> r = requests.get('https://api.github.com', auth=('user', 'pass'))
    >>> r.status_code
    204
    >>> r.headers['content-type']
    'application/json'
    >>> r.text
    ...

Zie `dezelfde code zonder Requests <https://gist.github.com/973705>`_.

Requests maakt het mogelijk om HTTP/1.1 verzoeken te versturen. Je kan headers (kopstukken), gegevens vanuit een formulier, een bestand wat uit meerdere delen is opgemaakt en parameters met eenvoudige Python associatieve-array's meesturen. Bovendien kan je de gegevens van de respons uitlezen. Dit wordt mogelijk gemaakt door httplib en `urllib3 <https://github.com/shazow/urllib3>`_, maar dan doet het zelf al het moeilijke werk en alle gekke hacks in plaats van dat je dat zelf moet doen.


Functionaliteiten
--------
- Internationale domeinen en URL's
- Verbinding levend houden & verbindingen uitwisselen
- Sessies met opslag van Cookie's
- SSL Verificatie in de stijl van Browser's
- Basic/Digest Authenticatie
- Elegante Sleutel/Waarde Cookies
- Automatische decompressie
- Unicode Respons
- Bestanden uit meerdere delen opgemaakt uploaden
- Verbinding Timeout
- Threadveiligheid


Installeren
------------

Om requests te installeren doe je:

.. code-block:: bash

    $ pip install requests

Of als het echt moet:

.. code-block:: bash

    $ easy_install requests

Maar eigenlijk zou je dat sowieso niet moeten doen.


Meedoen
----------

#. Kijk of er open issues zijn, of open een nieuwe issue om een discusie te beginnen over een nieuwe functionaliteit of een bug. Er is een label "Contributor Friendly" voor issues die ideaal kunnen dienen voor mensen die nog niet bekend zijn met de codebase.
#. Fork `de repo`_ op Github om je eigen verandering door te voeren op de **master** branch (or begin een nieuwe branch vanaf de master).
#. Schrijf een test die laat zien dat de bug opgelost is of dat de functionaliteit werkt zoals verwacht.
#. Stuur een pull request en val de maintainer lastig tot dat alles samengevoegd en gepubliceerd is. :) Oh en voeg jezelf vooral toe aan het AUTHORS_ bestand.

#. Write a test which shows that the bug was fixed or that the feature works as expected.
#. Send a pull request and bug the maintainer until it gets merged and published. :) Make sure to add yourself to AUTHORS_.

.. _`de repo`: http://github.com/kennethreitz/requests
.. _AUTHORS: https://github.com/kennethreitz/requests/blob/master/AUTHORS.rst
