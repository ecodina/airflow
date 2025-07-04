
 .. Licensed to the Apache Software Foundation (ASF) under one
    or more contributor license agreements.  See the NOTICE file
    distributed with this work for additional information
    regarding copyright ownership.  The ASF licenses this file
    to you under the Apache License, Version 2.0 (the
    "License"); you may not use this file except in compliance
    with the License.  You may obtain a copy of the License at

 ..   http://www.apache.org/licenses/LICENSE-2.0

 .. Unless required by applicable law or agreed to in writing,
    software distributed under the License is distributed on an
    "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
    KIND, either express or implied.  See the License for the
    specific language governing permissions and limitations
    under the License.

``apache-airflow-providers-edge3``
==================================


.. toctree::
    :hidden:
    :maxdepth: 1
    :caption: Basics

    Home <self>
    Changelog <changelog>
    Security <security>
    Why using Edge <why_edge>
    Architecture <architecture>
    Edge Worker Deployment <deployment>
    Edge UI Plugin <ui_plugin>
    Worker on Windows <install_on_windows>


.. toctree::
    :hidden:
    :maxdepth: 1
    :caption: Executors

    EdgeExecutor details <edge_executor>


.. toctree::
    :hidden:
    :maxdepth: 1
    :caption: References

    Configuration <configurations-ref>
    CLI <cli-ref>
    Python API <_api/airflow/providers/edge3/index>

.. toctree::
    :hidden:
    :maxdepth: 1
    :caption: Resources

    Example DAGs <_api/airflow/providers/edge3/example_dags/index>
    PyPI Repository <https://pypi.org/project/apache-airflow-providers-edge3/>
    Installing from sources <installing-providers-from-sources>

.. THE REMAINDER OF THE FILE IS AUTOMATICALLY GENERATED. IT WILL BE OVERWRITTEN AT RELEASE TIME!


.. toctree::
    :hidden:
    :maxdepth: 1
    :caption: Commits

    Detailed list of commits <commits>


apache-airflow-providers-edge3 package
------------------------------------------------------

Handle edge workers on remote sites via HTTP(s) connection and orchestrates work over distributed sites.

When tasks need to be executed on remote sites where the connection need to pass through
firewalls or other network restrictions, the Edge Worker can be deployed. The Edge Worker
is a lightweight process with reduced dependencies. The worker only needs to be able to
communicate with the central Airflow site via HTTPS.

In the central Airflow site the EdgeExecutor is used to orchestrate the work. The EdgeExecutor
is a custom executor which is used to schedule tasks on the edge workers. The EdgeExecutor can co-exist
with other executors (for example CeleryExecutor or KubernetesExecutor) in the same Airflow site.

Additional REST API endpoints are provided to distribute tasks and manage the edge workers. The endpoints
are provided by the API server.


Release: 1.1.1

Provider package
----------------

This package is for the ``edge3`` provider.
All classes for this package are included in the ``airflow.providers.edge3`` python package.

Installation
------------

You can install this package on top of an existing Airflow 2 installation via
``pip install apache-airflow-providers-edge3``.
For the minimum Airflow version supported, see ``Requirements`` below.

Requirements
------------

The minimum Apache Airflow version supported by this provider distribution is ``2.10.0``.

================================  ===================
PIP package                       Version required
================================  ===================
``apache-airflow``                ``>=2.10.0``
``apache-airflow-providers-fab``  ``>=1.5.3``
``pydantic``                      ``>=2.11.0``
``retryhttp``                     ``>=1.2.0,!=1.3.0``
================================  ===================

Cross provider package dependencies
-----------------------------------

Those are dependencies that might be needed in order to use all the features of the package.
You need to install the specified provider distributions in order to use them.

You can install such cross-provider dependencies when installing from PyPI. For example:

.. code-block:: bash

    pip install apache-airflow-providers-edge3[fab]


==============================================================================================  =======
Dependent package                                                                               Extra
==============================================================================================  =======
`apache-airflow-providers-fab <https://airflow.apache.org/docs/apache-airflow-providers-fab>`_  ``fab``
==============================================================================================  =======

Downloading official packages
-----------------------------

You can download officially released packages and verify their checksums and signatures from the
`Official Apache Download site <https://downloads.apache.org/airflow/providers/>`_

* `The apache-airflow-providers-edge3 1.1.1 sdist package <https://downloads.apache.org/airflow/providers/apache_airflow_providers_edge3-1.1.1.tar.gz>`_ (`asc <https://downloads.apache.org/airflow/providers/apache_airflow_providers_edge3-1.1.1.tar.gz.asc>`__, `sha512 <https://downloads.apache.org/airflow/providers/apache_airflow_providers_edge3-1.1.1.tar.gz.sha512>`__)
* `The apache-airflow-providers-edge3 1.1.1 wheel package <https://downloads.apache.org/airflow/providers/apache_airflow_providers_edge3-1.1.1-py3-none-any.whl>`_ (`asc <https://downloads.apache.org/airflow/providers/apache_airflow_providers_edge3-1.1.1-py3-none-any.whl.asc>`__, `sha512 <https://downloads.apache.org/airflow/providers/apache_airflow_providers_edge3-1.1.1-py3-none-any.whl.sha512>`__)
