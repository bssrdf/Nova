Getting Started
===============

The Nova library can be downloaded from `GitHub <https://github.com/>`_ using
the following command: ::

    git clone https://github.com/OrionQuest/Nova.git

Example projects that use the Nova core library live in a separate repository,
and can be downloaded using the following commands: ::

    cd Nova/Projects
    git clone https://github.com/OrionQuest/Nova_Examples.git

The build system uses `cmake <https://cmake.org/>`_ (version ``3.0`` or higher).
We recommend the use of the graphical version ``ccmake`` for easy configuration
of the environment variables. To compile, run the following commands in order: ::

    cd Nova
    mkdir build
    cd build
    ccmake ..

Set ``CMAKE_BUILD_TYPE`` to ``Release``, and turn on the following flags:
``ENABLE_ASSIMP_PLUGIN``, ``ENABLE_FREETYPE_PLUGIN``, ``ENABLE_GRID_PLUGIN``,
``ENABLE_TEXTFILERENDERER_PLUGIN``. As our first example, we will simulate
volumetric elastic objects, so turn on the corresponding project using the
following two additional flags: ``ENABLE_EMBEDDED_DEFORMABLES``,
``ENABLE_EMBEDDED_DEFORMABLES_PLUGIN``. Press ``c`` to configure, and then ``g``
to generate the ``Makefile``. Finally, run the following command: ::

    make -j 8

Nova depends on several libraries such as `GLM <https://glm.g-truc.net/0.9.9/index.html>`_, `Eigen <http://eigen.tuxfamily.org/index.php?title=Main_Page>`_,
`FreeType <https://www.freetype.org/>`_, `GLFW <http://www.glfw.org/>`_ (version ``3.0``), `GLEW <http://glew.sourceforge.net/>`_, `Boost <https://www.boost.org/>`_
(in particular, ``filesystem``, ``program_options``, and ``regex``), `Assimp <http://www.assimp.org/>`_, etc. Most of these libraries can be directly installed from the
package manager on Linux systems such as Ubuntu (version ``14.04`` or higher).
At the moment, the ``cmake`` files do not do a perfect job in finding all the missing libraries. We apologize for this slight inconvenience and will hopefully fix this in the near future.
