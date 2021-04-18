---
title: Poligoni tessellating
description: Poligoni tessellating
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilità OpenGL (GLU), a mosaico
- GLU (utilità OpenGL), mosaico
- Utilità OpenGL (GLU), poligoni semplici
- GLU (utilità OpenGL), poligoni semplici
- poligoni semplici OpenGL
- Utilità OpenGL (GLU), poligoni complessi
- GLU (utilità OpenGL), poligoni complessi
- poligoni complessi OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298814"
---
# <a name="tessellating-polygons"></a>Poligoni tessellating

OpenGL può visualizzare direttamente solo poligoni convessi semplici. Un poligono è semplice se:

-   I bordi si intersecano solo ai vertici.
-   Nessun vertice duplicato.
-   Esattamente due bordi sono conformi a qualsiasi vertice.

Per visualizzare semplici poligoni non convessi o poligoni semplici contenenti buchi, è necessario innanzitutto triangolare i poligoni (suddividerli in poligoni convessi). Tale suddivisione viene chiamata *mosaico*. GLU fornisce una raccolta di funzioni che eseguono lo schema a mosaico. Si noti che le funzioni a mosaico di GLU non possono gestire poligoni non semplici; non esiste un metodo OpenGL standard per gestire tali poligoni.

Poiché il mosaico è spesso necessario e può essere piuttosto complesso, in questa sezione vengono descritte in dettaglio le funzioni di suddivisione a mosaico di GLU. Queste funzioni accettano un poligono semplice di input arbitrario che potrebbe includere buchi, che restituiscono una combinazione di triangoli, mesh triangolari e ventole di triangolo. Se non si desidera gestire mesh o fan, è possibile specificare che le funzioni a mosaico restituiscano solo triangoli. Tuttavia, le informazioni sulla rete e sulla ventola migliorano le prestazioni. Le funzioni a mosaico poligono triangolano un poligono concavo con uno o più contorni.

**Per utilizzare la suddivisione a mosaico Polygon**

1.  Creare un oggetto a mosaico con [**gluNewTess**](glunewtess.md).
2.  Utilizzare [*gluTessCallBack*](glutess.md) per definire le funzioni di callback che si utilizzeranno per elaborare i triangoli generati da mosaico.
3.  Con [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), specificare il poligono con buchi o il Poligono concavo da tassellati.

    Quando la descrizione del poligono è completa, la struttura a mosaico richiama le funzioni di callback secondo necessità.

    È possibile eliminare gli oggetti mosaico non necessari con [**gluDeleteTess**](gludeletetess.md).

Per ulteriori informazioni sul salvataggio dei dati a mosaico, vedere [using callback Functions](using-callback-functions.md).

 

 




