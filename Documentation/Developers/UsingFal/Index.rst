.. ==================================================
.. FOR YOUR INFORMATION
.. --------------------------------------------------
.. -*- coding: utf-8 -*- with BOM.

.. include:: ../../Includes.txt


.. _using-fal:

Using FAL
^^^^^^^^^

This chapter explains the principles on how to use FAL in your extension and also inside the TYPO3 Core.
Additionally, it provides some useful examples for common use-cases

Use in FLUID
^^^^^^^^^^^^

Render images
~~~~~~~~~~~~~

**Direct rendering of images (TYPO3 >= 6.2):**

.. code-block:: fluid

  <f:for each="{files}" as="file">
    <f:image image="{file.image}" />
  </f:for>

**Rendering images with a max. width (TYPO3 >= 6.2):**

.. code-block:: fluid

  <f:for each="{files}" as="file">
    <f:image image="{file.image}" width="200m" />
  </f:for>
  

Create download link
~~~~~~~~~~~~~~~~~~~~

.. code-block:: fluid

  <f:for each="{files}" as="file">
    <a href="{file.originalResource.publicUrl}">{file.name}</a>
  </f:for>


