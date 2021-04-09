---
title: Specifica del poligono da tassellati
description: È possibile specificare un poligono, possibilmente contenente buchi, da tassellati usando
ms.assetid: 23e56d3e-c26c-4158-b0ce-cf8fcea22927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff36b74f9484a76f938a7a24847c218f5c4e8dbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955787"
---
# <a name="specifying-the-polygon-to-be-tessellated"></a>Specifica del poligono da tassellati

È possibile specificare un poligono, possibilmente contenente buchi, da tassellati utilizzando:

-   [**gluBeginPolygon**](glubeginpolygon.md)
-   [**gluTessVertex**](glutessvertex.md)
-   [**gluNextContour**](glunextcontour.md)
-   [**gluEndPolygon**](gluendpolygon.md)

Per i poligoni senza buchi, il processo di specifica è esattamente come in OpenGL:

1.  Iniziare a usare [**gluBeginPolygon**](glubeginpolygon.md).
2.  Chiamare [**gluTessVertex**](glutessvertex.md) per ogni vertice nel limite.
3.  Terminare il poligono con una chiamata a [**gluEndPolygon**](gluendpolygon.md).

Se un poligono è costituito da più contorni, inclusi buchi e buchi nei buchi, è necessario specificare i contorni uno dopo l'altro, prima di ogni [**gluNextContour**](glunextcontour.md). Quando si chiama [**gluEndPolygon**](gluendpolygon.md), viene segnalato il termine del contorno finale e viene avviato lo schema a mosaico. È possibile omettere la chiamata a **gluNextContour** prima del primo contorno. La funzione [**gluBeginPolygon**](glubeginpolygon.md) avvia la specifica di un poligono da tassellati e associa un oggetto a mosaico, **tessobj**, con esso. Le funzioni di callback da usare sono quelle che è possibile associare all'oggetto a mosaico con [*gluTessCallback*](glutess.md).

La funzione [**gluTessVertex**](glutessvertex.md) specifica un vertice nel poligono da tassellatire. Chiamare **gluTessVertex** per ogni vertice nel poligono. Il parametro *tessobj* della funzione è l'oggetto a mosaico da usare, *v* contiene le coordinate dei vertici tridimensionali e i *dati* sono un puntatore arbitrario che viene inviato al callback associato a **Glu \_ Vertex**. In genere, i *dati* contengono i dati dei vertici, le coordinate di trama, le informazioni sui colori o qualsiasi altro elemento necessario per l'applicazione.

La funzione [**gluNextContour**](glunextcontour.md) contrassegna l'inizio del contorno successivo quando più contorni costituiscono il limite del poligono da tassellati. Il parametro di *tipo* della funzione può **essere Glu \_ esterno**, **Glu \_ interno**, **Glu \_ CCW**, **Glu \_ CW** o **Glu \_ Unknown**. Queste costanti servono solo come hint per lo schema a mosaico. Se i risultati sono corretti, lo schema a mosaico potrebbe andare più velocemente. Se si ottengono errori, vengono ignorati e la suddivisione a mosaico funziona ancora.

Per un poligono con buchi, un contorno è il contorno esterno, mentre gli altri sono interni. Se non si chiama **gluNextContour** immediatamente dopo [**gluBeginPolygon**](glubeginpolygon.md), si presuppone che il primo contorno sia di tipo **Glu \_ esterno**.

**Glu \_ CW** e **Glu \_ CCW** indicano poligoni orientati in senso antiorario e in senso antiorario. La scelta in senso orario e in senso antiorario è arbitraria in tre dimensioni, ma in qualsiasi piano sono presenti due orientamenti diversi. usare in modo coerente i tipi **Glu \_ CW** e **Glu \_ CCW** . Usare **la \_ sconosciuta Glu** se non si sa quale usare.

La funzione [**gluEndPolygon**](gluendpolygon.md) indica la fine della specifica del poligono. Indica inoltre che lo schema a mosaico può iniziare a utilizzare l'oggetto a mosaico *tessobj*.

 

 




