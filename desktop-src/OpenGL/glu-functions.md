---
title: Funzioni GLU
description: Funzioni GLU
ms.assetid: 8304a291-1a26-42bc-8887-386732980722
keywords:
- Funzioni della libreria OpenGL, GLU
- Guida di riferimento a OpenGL, funzioni della libreria GLU
- Libreria GLU, funzioni
- Utilità OpenGL (GLU), funzioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fae3ece873f4e1e015861f597c0d51ebfc3436de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395722"
---
# <a name="glu-functions"></a>Funzioni GLU

Questa sezione include le pagine di riferimento, in ordine alfabetico, per tutte le funzioni della libreria di utilità OpenGL. Per informazioni generali su queste funzioni, vedere [OpenGL Utility Library](opengl-utility-library.md).



| Funzione                                                                                           | Descrizione                                                                                              |
|----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**gluBeginCurve**](glubegincurve.md), [ **gluEndCurve**](gluendcurve.md)                         | Delimita una definizione di curva B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) razionale non uniforme. |
| [**gluBeginPolygon**](glubeginpolygon.md), [ **gluEndPolygon**](gluendpolygon.md)                 | Delimitare una descrizione del poligono.                                                                           |
| [**gluBeginSurface**](glubeginsurface.md), [ **gluEndSurface**](gluendsurface.md)                 | Delimitare una definizione di superficie NURBS.                                                                      |
| [**gluBeginTrim**](glubegintrim.md), [ **gluEndTrim**](gluendtrim.md)                             | Delimitare una definizione del ciclo di troncamento NURBS.                                                                |
| [**gluBuild1DMipmaps**](glubuild1dmipmaps.md)                                                     | Crea mipmap 1-D.                                                                                     |
| [**gluBuild2DMipmaps**](glubuild2dmipmaps.md)                                                     | Crea mipmap 2D.                                                                                     |
| [**gluCylinder**](glucylinder.md)                                                                 | Disegna un cilindro.                                                                                        |
| [**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)                                           | Elimina definitivamente un oggetto NURBS.                                                                                 |
| [**gluDeleteQuadric**](gludeletequadric.md)                                                       | Elimina definitivamente un oggetto quadrica.                                                                               |
| [**gluDeleteTess**](gludeletetess.md)                                                             | Elimina definitivamente un oggetto a mosaico.                                                                          |
| [**gluDisk**](gludisk.md)                                                                         | Disegna un disco.                                                                                            |
| [**gluErrorString**](gluerrorstring.md)                                                           | Genera una stringa di errore da un codice di errore OpenGL o GLU. La stringa di errore è solo ANSI.                |
| [**gluGetNurbsProperty**](glugetnurbsproperty.md)                                                 | Recupera una proprietà NURBS.                                                                              |
| [**gluGetString**](glugetstring.md)                                                               | Recupera una stringa che descrive il numero di versione di GLU o le chiamate all'estensione GLU supportate.               |
| [**gluGetTessProperty**](glugettessproperty.md)                                                   | Recupera una proprietà dell'oggetto mosaico.                                                                |
| [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md)                                         | Carica matrici di campionamento e di eliminazione di NURBS.                                                               |
| [**gluLookAt**](glulookat.md)                                                                     | Definisce una trasformazione di visualizzazione.                                                                        |
| [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)                                                 | Crea un oggetto NURBS.                                                                                  |
| [**gluNewQuadric**](glunewquadric.md)                                                             | Crea un oggetto quadrica.                                                                                |
| [**gluNewTess**](glunewtess.md)                                                                   | Crea un oggetto a mosaico.                                                                           |
| [**gluNextContour**](glunextcontour.md)                                                           | Contrassegna l'inizio di un altro contorno.                                                                  |
| [*gluNurbsCallback*](glunurbs.md)                                                                 | Definisce un callback per un oggetto NURBS.                                                                   |
| [**gluNurbsCurve**](glunurbscurve.md)                                                             | Definisce la forma di una curva NURBS.                                                                      |
| [**gluNurbsProperty**](glunurbsproperty.md)                                                       | Imposta una proprietà NURBS.                                                                                   |
| [**gluNurbsSurface**](glunurbssurface.md)                                                         | Definisce la forma di una superficie NURBS.                                                                    |
| [**gluOrtho2D**](gluortho2d.md)                                                                   | Definisce una matrice di proiezione ortogonale 2D.                                                            |
| [**gluPartialDisk**](glupartialdisk.md)                                                           | Disegna un arco di un disco.                                                                                  |
| [**gluPerspective**](gluperspective.md)                                                           | Imposta una matrice di proiezione prospettica.                                                                 |
| [**gluPickMatrix**](glupickmatrix.md)                                                             | Definisce un'area di selezione.                                                                                |
| [**gluProject**](gluproject.md)                                                                   | Esegue il mapping delle coordinate dell'oggetto alle coordinate della finestra.                                                           |
| [**gluPwlCurve**](glupwlcurve.md)                                                                 | Descrive una curva di taglio NURBS lineare a tratti.                                                       |
| [*gluQuadricCallback*](gluquadric.md)                                                             | Definisce un callback per un oggetto quadrica.                                                                 |
| [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)                                                 | Specifica lo stile di estrazione desiderato per quadriche.                                                           |
| [**gluQuadricNormals**](gluquadricnormals.md)                                                     | Specifica il tipo di normali da usare per quadriche.                                              |
| [**gluQuadricOrientation**](gluquadricorientation.md)                                             | Specifica l'orientamento all'interno o all'esterno di quadriche.                                                    |
| [**gluQuadricTexture**](gluquadrictexture.md)                                                     | Specifica se il quadriche deve essere tramato.                                                           |
| [**gluScaleImage**](gluscaleimage.md)                                                             | Ridimensiona un'immagine a una dimensione arbitraria.                                                                    |
| [**gluSphere**](glusphere.md)                                                                     | Disegna una sfera.                                                                                          |
| [**gluTessBeginContour**](glutessbegincontour.md), [ **gluTessEndContour**](glutessendcontour.md) | Delimitare una descrizione del contorno.                                                                           |
| [**gluTessBeginPolygon**](glutessbeginpolygon.md), [ **gluTessEndPolygon**](glutessendpolygon.md) | Delimitare una descrizione del poligono.                                                                           |
| [*gluTessCallback*](glutess.md)                                                                   | Definisce un callback per un oggetto a mosaico.                                                            |
| [**gluTessNormal**](glutessnormal.md)                                                             | Specifica un normale per un poligono.                                                                        |
| [**gluTessProperty**](glutessproperty.md)                                                         | Imposta la proprietà di un oggetto a mosaico.                                                              |
| [**gluTessVertex**](glutessvertex.md)                                                             | Specifica un vertice in un poligono.                                                                         |
| [**gluUnProject**](gluunproject.md)                                                               | Esegue il mapping delle coordinate della finestra alle coordinate dell'oggetto.                                                           |



 

 

 




