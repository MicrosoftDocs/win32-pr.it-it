---
title: Utilizzo di funzioni di callback
description: Le funzioni di callback GLU, gluBeginPolygon, gluTessVertex, gluNextContour e gluEndPolygon, sono simili alle funzioni Polygon di OpenGL.
ms.assetid: e8277ba9-e270-4d7d-a29f-143f2f0d0324
keywords:
- Utilità OpenGL (GLU), funzioni di callback
- GLU (utilità OpenGL), funzioni di callback
- Utilità OpenGL (GLU), a mosaico
- GLU (utilità OpenGL), mosaico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a826d9416f94304762be2e840a3b6fea9ba458ec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855818"
---
# <a name="using-callback-functions"></a>Utilizzo di funzioni di callback

Le funzioni di callback GLU, [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), sono simili alle funzioni Polygon di OpenGL.

In genere salvano i dati per i triangoli, le mesh triangolari e le ventole triangolo nelle strutture di dati definite dall'utente o negli elenchi di visualizzazione OpenGL. Per eseguire il rendering dei poligoni, altro codice attraversa le strutture dei dati o chiama gli elenchi di visualizzazione. Sebbene le funzioni di callback possano chiamare funzioni OpenGL per visualizzare i poligoni direttamente, questa operazione non viene in genere eseguita, perché la suddivisione a mosaico può comportare un utilizzo intensivo di risorse di calcolo. È consigliabile salvare i dati se è possibile che si desideri visualizzarli nuovamente. Le funzioni di suddivisione a mosaico di GLU non restituiscono mai alcun nuovo vertice, quindi l'interpolazione di vertici, coordinate di trama o colori non è mai necessaria.

 

 




