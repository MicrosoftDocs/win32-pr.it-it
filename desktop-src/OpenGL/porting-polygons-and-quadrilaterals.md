---
title: Porting di poligoni e quadrilateri
description: 'Quando si portano poligoni e quadrilateri, tenere presenti i seguenti aspetti:'
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Porting di IRIS GL, quadrilateri
- porting da IRIS GL, quadrilateri
- porting in OpenGL da IRIS GL, quadrilateri
- Porting OpenGL da IRIS GL, quadrilateri
- funzioni di disegno, quadrilateri
- quadrilateri
- Porting di IRIS GL, poligoni
- porting da IRIS GL, poligoni
- porting in OpenGL da IRIS GL, poligoni
- Porting OpenGL da IRIS GL, poligoni
- funzioni di disegno, poligoni
- poligoni, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712502"
---
# <a name="porting-polygons-and-quadrilaterals"></a>Porting di poligoni e quadrilateri

Quando si portano poligoni e quadrilateri, tenere presenti i seguenti aspetti:

-   Non esiste un equivalente diretto per **concavo**(**true**). È invece possibile usare le routine a mosaico in GLU, descritte in [poligoni tessellating](tessellating-polygons.md).
-   Le modalità poligono sono impostate in modo diverso.
-   Queste funzioni di disegno Polygon non hanno equivalenti diretti in OpenGL: la famiglia **Poly** di routine; famiglia di routine **POLF** . **PMV**, **PDR** e **PCLOS**; **rpmv** e **rpdr**; **splf**; e **spclos**.

Se il codice di IRIS GL usa queste funzioni, sarà necessario riscrivere il codice usando [**glBegin**](glbegin.md)(GL \_ Polygon).

La tabella seguente elenca le funzioni di disegno del poligono IRIS GL e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL         | OpenGL (funzione)                                                    | Significato                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| **bgnpolygonendpolygon** | [**glBegin**](glbegin.md) ( \_ poligono GL)[**glEnd**](glend.md)   | I vertici definiscono il limite di un poligono convesso semplice.    |
|                          | **glBegin**(GL \_ quad)**glEnd**<br/>                       | Interpreta le quadruple dei vertici come quadrilateri.    |
| **bgnqstripendqstrip**   | [**glBegin**](glbegin.md) (GL \_ Quad \_ Strip)**glEnd**<br/> | Interpreta i vertici come strisce collegate di quadrilateri. |
|                          | [glEdgeFlag](gledgeflag-functions.md)                             |                                                         |
| **modalità multifunzione**             | [**glPolygonMode**](glpolygonmode.md)                             | Imposta la modalità di disegno poligono.                              |
| **rectrectf**<br/> | [glRect](glrect-functions.md)                                     | Disegna un rettangolo.                                      |
| **sboxsboxf**<br/> |                                                                    | Disegna un rettangolo allineato allo schermo.                       |



 

??

## <a name="porting-polygon-modes"></a>Modalità poligono di porting

La funzione OpenGL [**glPolygonMode**](glpolygonmode.md) consente di specificare il lato di un poligono (back o front) a cui si applica la modalità. La relativa sintassi è la seguente:

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

dove Face è uno dei seguenti:



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| \_primo piano GL            | modalità che si applica ai poligoni in primo piano                |
| indietro per GL \_             | modalità applicabile ai poligoni sottoposti a back-end                 |
| \_primo \_ e \_ indietro GL | modalità che si applica sia ai poligoni anteriori che al back-end |



 

La \_ modalità Front \_ e \_ back GL è equivalente alla funzione di **polimodalità** di Iris GL. La tabella seguente elenca le modalità poligono di IRIS GL e le modalità OpenGL equivalenti.



| Modalità di IRIS GL | Modalità OpenGL | Significato                                       |
|--------------|-------------|-----------------------------------------------|
| punto di PYM \_   | \_punto GL   | Disegna i vertici come punti.                     |
| \_linea Pym    | \_linea GL    | Disegna i bordi del limite come segmenti di linea.        |
| \_riempimento Pym    | \_riempimento GL    | Disegna il riempimento interno del poligono.                |
| PYM \_ Hollow  |             | Riempie solo i pixel interni ai limiti. |



 

## <a name="porting-polygon-stipples"></a>Porting poligono Stipples

Quando si esegue il porting di IRIS GL Polygon stipples, tenere presente quanto segue:

-   OpenGL non usa le tabelle per poligono stipples; viene mantenuto solo un modello stipple. È possibile usare gli elenchi di visualizzazione per archiviare modelli stipple diversi.
-   La dimensione bitmap stipple del poligono OpenGL è sempre un modello di bit 32x32.
-   La codifica stipple è interessata da [**glPixelStore**](glpixelstore-functions.md).

Per altre informazioni sul porting del poligono stipples, vedere [porting pixel Operations](porting-pixel-operations.md).

La tabella seguente elenca le funzioni stipple di IRIS GL Polygon e le relative funzioni OpenGL equivalenti.



| Funzione IRIS GL | OpenGL (funzione)                                    | Significato                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| **defpattern**   | [**glPolygonStipple**](glpolygonstipple.md)       | Imposta il pattern stipple.                             |
| **criteri di ricerca**   |                                                    | OpenGL mantiene solo un modello stipple poligono.        |
| **GetPattern**   | [**glGetPolygonStipple**](glgetpolygonstipple.md) | Restituisce la bitmap stipple (utilizzata per restituire un indice). |



 

In OpenGL è possibile abilitare e disabilitare poligono punteggiatura passando GL \_ Polygon \_ stipple come parametro per [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).

Nell'esempio di codice OpenGL seguente viene illustrato il poligono punteggiatura:


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a>Porting di poligoni tassellati

In IRIS GL usare **concavo**(**true**) e quindi **bgnpolygon** per creare poligoni concavi. OpenGL GLU include funzioni che è possibile usare per creare poligoni concavi.

**Per creare un poligono concavo con OpenGL**

1.  Creare un oggetto a mosaico.
2.  Definire callback che saranno usati per elaborare i triangoli generati da mosaico.
3.  Specificare il Poligono concavo da tassellati.

La tabella seguente elenca le funzioni OpenGL per il disegno di poligoni tassellati.



| Funzione OpenGL GLU                        | Significato                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [**gluNewTess**](glunewtess.md)           | Crea un nuovo oggetto a mosaico.                                 |
| [**gluDeleteTess**](gludeletetess.md)     | Elimina un oggetto a mosaico.                                     |
| [*gluTessCallback*](glutess.md)           |                                                                    |
| [**gluBeginPolygon**](glubeginpolygon.md) | Inizia la specifica del poligono.                                  |
| [**gluTessVertex**](glutessvertex.md)     | Specifica un vertice del poligono in un contorno.                           |
| [**gluNextContour**](glunextcontour.md)   | Indica che la serie successiva di vertici descrive un nuovo contorno. |
| [**gluEndPolygon**](gluendpolygon.md)     | Termina la specifica del poligono.                                    |



 

 

 





