---
title: Dati di input
description: Per la pipeline OpenGL è necessario inserire diversi tipi di dati
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Pipeline di elaborazione OpenGL, dati di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298057"
---
# <a name="input-data"></a>Dati di input

Per la pipeline OpenGL è necessario inserire diversi tipi di dati:

-   **Vertici**. I vertici descrivono la forma dell'oggetto geometrico desiderato. Per specificare i vertici, usare le funzioni [**glVertex \***](glvertex-functions.md) insieme a [**glBegin**](glbegin.md) e [**glEnd**](glend.md) per creare un punto, una linea o un poligono. È anche possibile usare [**glRect**](glrect-functions.md) per descrivere un intero rettangolo in una sola volta.
-   **Flag Edge**. Per impostazione predefinita, tutti i bordi dei poligoni sono bordi limite. Usare [**glEdgeFlag \***](gledgeflag-functions.md) per impostare in modo esplicito il flag Edge.
-   **Posizione raster corrente**. Specificata con [**glRasterPos \***](glrasterpos-functions.md), la posizione raster corrente viene usata per determinare le coordinate raster per le operazioni di disegno pixel e bitmap.
-   **Normale corrente**. Un vettore normale associato a un vertice particolare determina il modo in cui una superficie a tale vertice è orientata allo spazio tridimensionale. Ciò a sua volta influiscono sulla quantità di luce ricevuta da un vertice specifico. Usare [**glNormal \***](glnormal-functions.md) per specificare un vettore normale.
-   **Colore corrente**. Il colore di un vertice, insieme alle condizioni di illuminazione, determina il colore finale illuminato. Il colore viene specificato [**con \* glColor**](glcolor-functions.md) se in modalità RGBA o con [**glIndex \***](glindex-functions.md) se si trova in modalità di indice a colori.
-   **Coordinate di trama correnti**. Specificata con [**glTexCoord \***](gltexcoord-functions.md), le coordinate di trama determinano la posizione in una mappa di trama da associare a un vertice di un oggetto.

> [!Note]  
> Quando viene chiamato **glVertex \*** , il vertice risultante eredita il flag del bordo, il normale, il colore e le coordinate di trama correnti. Pertanto, **glEdgeFlag \***, **glNormal \***, **glColor \*** e **\* glTexCoord** devono essere chiamati prima di **glVertex \***, se hanno effetto sul vertice risultante.

 

 

 




