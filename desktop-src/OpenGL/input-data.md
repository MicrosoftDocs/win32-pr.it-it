---
title: Dati di input
description: La pipeline OpenGL richiede l'immissione di diversi tipi di dati
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Pipeline di elaborazione OpenGL, dati di input
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a588e60991ad068653890659e236f8a7a96e62cad524b13ea72bfd38fb5bba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937428"
---
# <a name="input-data"></a>Dati di input

La pipeline OpenGL richiede l'immissione di diversi tipi di dati:

-   **Vertici**. I vertici descrivono la forma dell'oggetto geometrico desiderato. Per specificare i vertici, usare le funzioni [ * *glVertex \** _](glvertex-functions.md) in combinazione con _ [*glBegin* *](glbegin.md) e [**glEnd**](glend.md) per creare un punto, una linea o un poligono. È anche possibile usare [**glRect**](glrect-functions.md) per descrivere un intero rettangolo contemporaneamente.
-   **Flag edge**. Per impostazione predefinita, tutti i bordi dei poligoni sono bordi limite. Usare [**glEdgeFlag per \***](gledgeflag-functions.md) impostare in modo esplicito il flag edge.
-   **Posizione raster corrente.** Specificato con [**glRasterPos \***](glrasterpos-functions.md), la posizione raster corrente viene usata per determinare le coordinate raster per le operazioni di disegno con pixel e bitmap.
-   **Normale corrente.** Un vettore normale associato a un vertice specifico determina come una superficie in tale vertice è orientata nello spazio tridimensionale; ciò influisce a sua volta sulla quantità di luce ricevuta da un vertice specifico. Usare [**glNormal \***](glnormal-functions.md) per specificare un vettore normale.
-   **Colore corrente.** Il colore di un vertice, insieme alle condizioni di illuminazione, determina il colore finale acceso. Color viene specificato con [ * *glColor \** _](glcolor-functions.md) se in modalità RGBA o con _ [*glIndex \** *](glindex-functions.md) se in modalità color-index.
-   **Coordinate correnti della trama.** Specificate con [**glTexCoord, \***](gltexcoord-functions.md)le coordinate della trama determinano la posizione in una mappa di trama da associare a un vertice di un oggetto.

> [!Note]  
> Quando viene chiamato glVertex _, il vertice risultante eredita il flag del bordo corrente, le coordinate **\* *normali, di colore e di trama. Pertanto, _* glEdgeFlag \* *_, _* glNormal \* *_, _* glColor _, e \* *_* glTexCoord _ \*  \*** devono essere chiamati prima di _ glVertex , se devono influire sul vertice risultante.

 

 

 




