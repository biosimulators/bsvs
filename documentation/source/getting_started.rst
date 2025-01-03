Getting Started
===============

Installation
------------
The easiest way to install BioCompose is using pip:

.. code-block:: bash

    pip install bsvs

Verification
------------
Running a verification with `bsvs` can be achieved in a few simple steps.

Running **OMEX verifications**:

.. code-block:: python

    import bsvs

    filepath = '/path/to/a/valid/omex/file.omex'

    verification = bc.verify(filepath)

Running **SBML verifications**:

.. code-block:: python

    import bsvs

    filepath = '/path/to/a/valid/sbml/file.xml'
    start_time = 0
    duration = 100
    n_steps = 1000

    verification = bsvs.verify(filepath, start_time, duration, n_steps)

Visualizing verifications:

.. code-block:: python

    verification.get_output_observables()  # visualize observables
    verification.get_rmse(save_dest='/my/save/path/for/observables')  # visualize root-mean-square error scores for all simulators involved in the verification.

Verifications for OMEX can also be executed using the command-line interface which is installed with the package:

.. code-block:: bash

    verify /path/to/a/valid/omex/file.omex