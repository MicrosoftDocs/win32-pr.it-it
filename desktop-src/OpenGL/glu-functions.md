---
title: Funzioni GLU
description: Funzioni GLU
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- Funzioni della libreria OpenGL,GLU
- Informazioni di riferimento su OpenGL, funzioni della libreria GLU
- libreria GLU, funzioni
- Utilità OpenGL (GLU),funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4483b364d2d67daff0bbc04b9a30cd7cdb3059f3977f763b247f77be74d62f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777701"
---
# <a name="glu-functions"></a>Funzioni GLU

Questa sezione include pagine di riferimento, in ordine alfabetico, per tutte le funzioni della libreria di utilità OpenGL. Per informazioni di base su queste funzioni, vedere [OpenGL Utility Library.](opengl-utility-library.md)



| Funzione                                                                                           | Descrizione                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**gluBeginCurve**](glubegincurve.md), [ **gluEndCurve**](gluendcurve.md)                         | Delimitare una definizione di curva B-Spline razionale non uniforme[(NURBS).](using-nurbs-curves-and-surfaces.md) |
| [**gluBeginPolygon**](glubeginpolygon.md), [ **gluEndPolygon**](gluendpolygon.md)                 | Delimitare una descrizione del poligono.                                                                           |
| [**gluBeginSurface**](glubeginsurface.md), [ **gluEndSurface**](gluendsurface.md)                 | Delimitare una definizione di superficie NURBS.                                                                      |
| [**gluBeginTrim**](glubegintrim.md), [ **gluEndTrim**](gluendtrim.md)                             | Delimitare una definizione di ciclo di taglio NURBS.                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | Crea mipmap 1D.                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | Crea mipmap 2D.                                                                                     |
| [**gluCylinder**](glucylinder.md)                                                                 | Disegna un cilindro.                                                                                        |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)                                           | Elimina un oggetto NURBS.                                                                                 |
| [**gluDeleteQuadric**](gludeletequadric.md)                                                       | Elimina un oggetto quadric.                                                                               |
| [**gluDeleteTess**](gludeletetess.md)                                                             | Elimina un oggetto a tessellazione.                                                                          |
| [**gluDisk**](gludisk.md)                                                                         | Disegna un disco.                                                                                            |
| [**gluErrorString**](gluerrorstring.md)                                                           | Genera una stringa di errore da un codice di errore OpenGL o GLU. La stringa di errore è solo ANSI.                |
| [**gluGetNurbsProperty**](glugetnurbsproperty.md)                                                 | Recupera una proprietà NURBS.                                                                              |
| [**gluGetString**](glugetstring.md)                                                               | Recupera una stringa che descrive il numero di versione GLU o le chiamate all'estensione GLU supportate.               |
| [**gluGetTessProperty**](glugettessproperty.md)                                                   | Recupera una proprietà dell'oggetto a tessellazione.                                                                |
| [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)                                         | Carica le matrici di campionamento e di culling NURBS.                                                               |
| [**gluLookAt**](glulookat.md)                                                                     | Definisce una trasformazione di visualizzazione.                                                                        |
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)                                                 | Crea un oggetto NURBS.                                                                                  |
| [**gluNewQuadric**](glunewquadric.md)                                                             | Crea un oggetto quadric.                                                                                |
| [**gluNewTess**](glunewtess.md)                                                                   | Crea un oggetto a tessellazione.                                                                           |
| [**gluNextContour**](glunextcontour.md)                                                           | Contrassegna l'inizio di un altro contorno.                                                                  |
| [*gluNurbsCallback*](glunurbs.md)                                                                 | Definisce un callback per un oggetto NURBS.                                                                   |
| [**gluNurbsCurve**](glunurbscurve.md)                                                             | Definisce la forma di una curva NURBS.                                                                      |
| [**gluNurbsProperty**](glunurbsproperty.md)                                                       | Imposta una proprietà NURBS.                                                                                   |
| [**gluNurbsSurface**](glunurbssurface.md)                                                         | Definisce la forma di una superficie NURBS.                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | Definisce una matrice di proiezione ortogonale 2D.                                                            |
| [**gluPartialDisk**](glupartialdisk.md)                                                           | Disegna un arco di un disco.                                                                                  |
| [**gluPerspective**](gluperspective.md)                                                           | Imposta una matrice di proiezione prospettica.                                                                 |
| [**gluPickMatrix**](glupickmatrix.md)                                                             | Definisce un'area di selezione.                                                                                |
| [**gluProject**](gluproject.md)                                                                   | Mappe coordinate dell'oggetto alle coordinate della finestra.                                                           |
| [**gluPwlCurve**](glupwlcurve.md)                                                                 | Descrive una curva di taglio NURBS lineare a punti.                                                       |
| [*gluQuadricCallback*](gluquadric.md)                                                             | Definisce un callback per un oggetto quadric.                                                                 |
| [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)                                                 | Specifica lo stile di disegno desiderato per i quadrifoli.                                                           |
| [**gluQuadricNormals**](gluquadricnormals.md)                                                     | Specifica il tipo di normali da usare per i quadrifoli.                                              |
| [**gluQuadricOrientation**](gluquadricorientation.md)                                             | Specifica l'orientamento interno o esterno per i quadrifoli.                                                    |
| [**gluQuadricTexture**](gluquadrictexture.md)                                                     | Specifica se è necessario eseguire la trama dei quadrici.                                                           |
| [**gluScaleImage**](gluscaleimage.md)                                                             | Ridimensiona un'immagine a una dimensione arbitraria.                                                                    |
| [**gluSphere**](glusphere.md)                                                                     | Disegna una sfera.                                                                                          |
| [**gluTessBeginContour**](glutessbegincontour.md), [ **gluTessEndContour**](glutessendcontour.md) | Delimitare una descrizione del contorno.                                                                           |
| [**gluTessBeginPolygon**](glutessbeginpolygon.md), [ **gluTessEndPolygon**](glutessendpolygon.md) | Delimitare una descrizione del poligono.                                                                           |
| [*gluTessCallback*](glutess.md)                                                                   | Definisce un callback per un oggetto a tessellazione.                                                            |
| [**gluTessNormal**](glutessnormal.md)                                                             | Specifica una normale per un poligono.                                                                        |
| [**GluTessProperty**](glutessproperty.md)                                                         | Imposta la proprietà di un oggetto a tessellazione.                                                              |
| [**gluTessVertex**](glutessvertex.md)                                                             | Specifica un vertice su un poligono.                                                                         |
| [**gluUnProject**](gluunproject.md)                                                               | Mappe coordinate della finestra alle coordinate dell'oggetto.                                                           |



 

 

 




