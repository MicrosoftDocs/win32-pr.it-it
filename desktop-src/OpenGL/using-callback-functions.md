---
title: Uso di funzioni di callback
description: Le funzioni di callback GLU, gluBeginPolygon, gluTessVertex, gluNextContour e gluEndPolygon, sono simili alle funzioni poligono OpenGL.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- Utilità OpenGL (GLU), funzioni di callback
- GLU (utilità OpenGL), funzioni di callback
- Utilità OpenGL (GLU), a tessellazione
- GLU (utilità OpenGL), a tessellazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75556b8c366c83df5a5976c867e6fc5f68d520da65ed8f34609f312cbfebaa7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932896"
---
# <a name="using-callback-functions"></a>Uso di funzioni di callback

Le funzioni di callback GLU, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), sono simili alle funzioni poligono OpenGL.

In genere salvano i dati per i triangoli, le mesh dei triangoli e le ventole dei triangoli in strutture di dati definite dall'utente o negli elenchi di visualizzazione OpenGL. Per eseguire il rendering dei poligoni, altro codice attraversa le strutture dei dati o chiama gli elenchi di visualizzazione. Anche se le funzioni di callback possono chiamare funzioni OpenGL per visualizzare direttamente i poligoni, questa operazione in genere non viene eseguita, perché la tessellazione può essere a elevato utilizzo di risorse dal punto di vista del calcolo. È buona idea salvare i dati se è possibile visualizzarli di nuovo. Le funzioni glu a trama non restituiscono mai nuovi vertici, pertanto l'interpolazione di vertici, coordinate di trama o colori non è mai necessaria.

 

 




