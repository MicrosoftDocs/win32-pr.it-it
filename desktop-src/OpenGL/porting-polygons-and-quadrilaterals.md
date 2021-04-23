---
title: Porting di poligoni e quadrilateri
description: Tenere presente quanto segue durante la portabilità di poligoni e quadrilateri
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Portabilità IRIS GL, quadrilaterali
- porting da IRIS GL, quadrilaterali
- porting to OpenGL from IRIS GL,quadrilaterals
- Portabilità OpenGL da IRIS GL, quadrilaterali
- funzioni di disegno, quadrilaterali
- Quadrilateri
- Portabilità IRIS GL, poligoni
- porting da IRIS GL, poligoni
- porting to OpenGL from IRIS GL,polygons
- Portabilità OpenGL da IRIS GL, poligoni
- funzioni di disegno, poligoni
- poligoni, porting da IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908459"
---
# <a name="porting-polygons-and-quadrilaterals"></a>Porting di poligoni e quadrilateri

Quando si esegue la portabilità di poligoni e quadrilateri, tenere presente quanto segue:

-   Non esiste alcun equivalente diretto per **concave**(**TRUE**). È invece possibile usare le routine a tessellazione in GLU, descritte in [Tessellating Polygons](tessellating-polygons.md).
-   Le modalità poligono sono impostate in modo diverso.
-   Queste funzioni di disegno poligono non hanno equivalenti diretti in OpenGL: la **famiglia** poli di routine; la famiglia di routine **polf;** **pmv**, **pdr** e **pclos**; **rpmv** e **rpdr**; **splf**; e **spclos**.

Se il codice IRIS GL usa queste funzioni, sarà necessario riscrivere il codice usando [**glBegin**](glbegin.md)( GL \_ POLYGON ).

Nella tabella seguente sono elencate le funzioni di disegno poligono IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS         | Funzione OpenGL                                                    | Significato                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| **bgnpolygonendpolygon** | [**glBegin**](glbegin.md) ( GL \_ POLYGON )[**glEnd**](glend.md)   | I vertici definiscono il limite di un poligono convesso semplice.    |
|                          | **glBegin**( GL \_ QUADS )**glEnd**<br/>                       | Interpreta i quadrilateri dei vertici come quadrilaterali.    |
| **bgnqstripendqstrip**   | [**glBegin**](glbegin.md) ( GL \_ QUAD STRIP ) \_ **glEnd**<br/> | Interpreta i vertici come strisce collegate di quadrilaterali. |
|                          | [glEdgeFlag](gledgeflag-functions.md)                             |                                                         |
| **polymode**             | [**glPolygonMode**](glpolygonmode.md)                             | Imposta la modalità di disegno poligono.                              |
| **rectrectf**<br/> | [glRect](glrect-functions.md)                                     | Disegna un rettangolo.                                      |
| **sboxsboxf**<br/> |                                                                    | Disegna un rettangolo allineato a schermo.                       |



 

??

## <a name="porting-polygon-modes"></a>Portabilità delle modalità poligono

La funzione OpenGL [**glPolygonMode**](glpolygonmode.md) consente di specificare a quale lato di un poligono (la parte posteriore o anteriore) si applica la modalità. La relativa sintassi è la seguente:

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

dove face è uno dei seguenti:



|Valore GLenum                      |  Significato                                                          |
|----------------------|------------------------------------------------------------|
| GL \_ FRONT            | modalità che si applica ai poligoni rivolti anteriore                |
| GL \_ BACK             | modalità che si applica ai poligoni rivolti all'indietro                 |
| GL \_ FRONT \_ AND \_ BACK | modalità che si applica sia ai poligoni anteriore che a quello posteriore |



 

La modalità \_ GL FRONT E BACK è equivalente alla funzione \_ \_ **polimode** IRIS GL. La tabella seguente elenca le modalità poligono IRIS GL e le modalità OpenGL equivalenti.



| Modalità GL IRIS | Modalità OpenGL | Significato                                       |
|--------------|-------------|-----------------------------------------------|
| PYM \_ POINT   | PUNTO \_ GL   | Disegna i vertici come punti.                     |
| PYM \_ LINE    | GL \_ LINE    | Disegna i bordi dei limiti come segmenti di linea.        |
| RIEMPIMENTO \_ PYM    | GL \_ FILL    | Disegna il riempimento interno del poligono.                |
| PYM \_ INSODEME  |             | Riempie solo i pixel interni ai limiti. |



 

## <a name="porting-polygon-stipples"></a>Porting Polygon Stipples

Quando si esegue il porting degli stipple poligoni IRIS GL, tenere presenti i punti seguenti:

-   OpenGL non usa tabelle per gli stipples poligonali. viene mantenuto un solo modello di punta. È possibile usare elenchi di visualizzazione per archiviare modelli di stili diversi.
-   La dimensione della bitmap dello stipple poligono OpenGL è sempre un modello a 32x32 bit.
-   La codifica Stipple è interessata [**da glPixelStore**](glpixelstore-functions.md).

Per altre informazioni sul porting degli stipples poligoni, vedere Porting Pixel Operations ( [Porting Pixel Operations](porting-pixel-operations.md)).

Nella tabella seguente sono elencate le funzioni di punta del poligono IRIS GL e le funzioni OpenGL equivalenti.



| Funzione GL IRIS | Funzione OpenGL                                    | Significato                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| **defpattern**   | [**glPolygonStipple**](glpolygonstipple.md)       | Imposta il modello di stipla.                             |
| **setpattern**   |                                                    | OpenGL mantiene un solo motivo a punta poligono.        |
| **Getpattern**   | [**glGetPolygonStipple**](glgetpolygonstipple.md) | Restituisce la bitmap stipple (usata per restituire un indice). |



 

In OpenGL si abilita e disabilita lo stippling dei poligoni passando GL POLYGON STIPPLE come parametro \_ \_ per [**glEnable**](glenable.md) e [**glDisable.**](gldisable.md)

L'esempio di codice OpenGL seguente illustra lo stippling dei poligoni:


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



## <a name="porting-tessellated-polygons"></a>Portabilità di poligoni a tessellatura

In IRIS GL si usa **concave**(**TRUE**) e quindi **bgnpolygon** per disegnare poligoni concavi. OpenGL GLU include funzioni che è possibile usare per disegnare poligoni concavi.

**Per disegnare un poligono concavo con OpenGL**

1.  Creare un oggetto a tessellazione.
2.  Definire i callback che verranno usati per elaborare i triangoli generati dal tessellatore.
3.  Specificare il poligono concavo da a tessire.

Nella tabella seguente sono elencate le funzioni OpenGL per il disegno di poligoni a colonne.



| Funzione GLU OpenGL                        | Significato                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [**gluNewTess**](glunewtess.md)           | Crea un nuovo oggetto a tessellazione.                                 |
| [**gluDeleteTess**](gludeletetess.md)     | Elimina un oggetto a tessellazione.                                     |
| [*gluTessCallback*](glutess.md)           |                                                                    |
| [**gluBeginPolygon**](glubeginpolygon.md) | Avvia la specifica del poligono.                                  |
| [**gluTessVertex**](glutessvertex.md)     | Specifica un vertice poligonale in un contorno.                           |
| [**gluNextContour**](glunextcontour.md)   | Indica che la serie successiva di vertici descrive un nuovo contorno. |
| [**gluEndPolygon**](gluendpolygon.md)     | Termina la specifica del poligono.                                    |



 

 

 





