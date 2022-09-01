


# lib_CadViewer

CADViewer component for Convertigo platform. This component can add 2D Plans and annotation features to your convertigo projects

This Componend is based on the CADViewer provided by tailormade.

(https://www.tailormade.com/products/cadviewer)




For more technical informations : [documentation](./project.md)

- [Installation](#installation)
- [Sequences](#sequences)
    - [ConvertToSvg](#converttosvg)
    - [UploadDrawing](#uploaddrawing)
- [Mobile Library](#mobile-library)
    - [Shared Components](#shared-components)
        - [CadViewer](#cadviewer)


## Installation

1. In your Convertigo Studio use `File->Import->Convertigo->Convertigo Project` and hit the `Next` button
2. In the dialog `Project remote URL` field, paste the text below:
   <table>
     <tr><td>Usage</td><td>Click the copy button</td></tr>
     <tr><td>To contribute</td><td>

     ```
     lib_CadViewer=https://github.com/convertigo/c8oprj-lib-cadviewer.git:branch=master
     ```
     </td></tr>
     <tr><td>To simply use</td><td>

     ```
     lib_CadViewer=https://github.com/convertigo/c8oprj-lib-cadviewer/archive/master.zip
     ```
     </td></tr>
    </table>
3. Click the `Finish` button. This will automatically import the __lib_CadViewer__ project


## Sequences

### ConvertToSvg

Uses the AX Converter to Convert DWG drwings to SVG

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>input</td><td>The input file (relative to the project/data directory)</td>
</tr>
<tr>
<td>output</td><td>The output file (relative to the project/data directory)</td>
</tr>
</table>

### UploadDrawing

Upload & Converts a DWG drawing to SVG, then stores it in the database

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>drawingFile</td><td>The Drawing file in DWG format as a File Upload</td>
</tr>
</table>

## Mobile Library

Describes the mobile application global properties

### Shared Components

#### CadViewer

The OffLine CADViewer component is based on CADViewer  https://www.cadviewer.com/ 

This component wil display and enable to annotate drawings from a fullsync database. Before using this compoent, you must insert drawings in the FS database using the :

- UploadDrawing sequence

The Drawings will be converted to the correct SVG format and Stored as attachements in the database.

On the client side, you  sould sync the data to you device and use the CADViewer component providing the database name and the drawing name






**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>database</td><td>the Fullsync databse name to get drawings from</td>
</tr>
<tr>
<td>drawing</td><td>The drawing name to display</td>
</tr>
</table>



