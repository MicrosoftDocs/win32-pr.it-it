---
title: Poligoni a tessellazione
description: Poligoni a tessellazione
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilità OpenGL (GLU), a tessellazione
- GLU (utilità OpenGL), a tessellazione
- Utilità OpenGL (GLU), poligoni semplici
- GLU (utilità OpenGL), poligoni semplici
- poligoni semplici OpenGL
- Utilità OpenGL (GLU), poligoni complessi
- GLU (utilità OpenGL), poligoni complessi
- poligoni complessi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948e0669348404af763883f7ff713212d52f6f0d79312812552c0e5053041627
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034513"
---
# <a name="tessellating-polygons"></a>Poligoni a tessellazione

OpenGL può visualizzare direttamente solo poligoni convessi semplici. Un poligono è semplice se:

-   I bordi si intersecano solo in corrispondenza dei vertici.
-   Non sono presenti vertici duplicati.
-   Esattamente due bordi si incontrano in qualsiasi vertice.

Per visualizzare semplici poligoni non convessi o poligoni semplici contenenti fori, è prima necessario triangolare i poligoni (suddividerli in poligoni convessi). Tale suddivisione è detta *suddivisione a tessellazione.* GLU fornisce una raccolta di funzioni che eseguono la tessellazione. Si noti che le funzioni a tessellazione GLU non possono gestire poligoni nonsimple. non esiste alcun metodo OpenGL standard per gestire tali poligoni.

Poiché la tessellazione è spesso necessaria e può essere piuttosto difficile, in questa sezione vengono descritte in dettaglio le funzioni a tessellazione GLU. Queste funzioni accettano come input poligoni semplici arbitrari che potrebbero includere fori e restituiscono una combinazione di triangoli, mesh di triangoli e ventole di triangolo. Se non si vogliono gestire mesh o ventole, è possibile specificare che le funzioni a trama restituiscono solo triangoli. Tuttavia, le informazioni su mesh e ventole migliorano le prestazioni. Le funzioni a tessellazione poligono triangolano un poligono concavo con uno o più contorni.

**Per usare la tessellazione poligonale**

1.  Creare un oggetto a tessellazione [**con gluNewTess**](glunewtess.md).
2.  Usare [*gluTessCallBack*](glutess.md) per definire le funzioni di callback che verranno usate per elaborare i triangoli generati dal tessellatore.
3.  Con [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), specificare il poligono con fori o il poligono concavo da a tessellare.

    Al termine della descrizione del poligono, la struttura a tessellazione richiama le funzioni di callback in base alle esigenze.

    È possibile eliminare gli oggetti a tessellazione non necessario [**con gluDeleteTess**](gludeletetess.md).

Per altre informazioni sul salvataggio dei dati a tassellamento, vedere [Uso delle funzioni di callback](using-callback-functions.md).

 

 




