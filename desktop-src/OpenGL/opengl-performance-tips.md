---
title: Suggerimenti sulle prestazioni di OpenGL
description: Suggerimenti sulle prestazioni di OpenGL
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL, suggerimenti sulle prestazioni
- OpenGL, procedure consigliate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e5b6fa33f8d6841d0fd47d1a655ef99facc84e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710594"
---
# <a name="opengl-performance-tips"></a>Suggerimenti sulle prestazioni di OpenGL

Queste procedure di programmazione ottimizzano le prestazioni dell'applicazione:

-   Usare [**glColorMaterial**](glcolormaterial.md) quando viene variata rapidamente una sola proprietà Material (a ogni vertice, ad esempio). Usare [**glMaterial**](glmaterial-functions.md) per le modifiche non frequenti o quando più di una proprietà del materiale singolo viene variata rapidamente.
-   Usare [**glLoadIdentity**](glloadidentity.md) per inizializzare una matrice, anziché caricare la propria copia della matrice di identità.
-   Usare chiamate a matrici specifiche, ad esempio [**glRotate**](glrotate.md), [**glTranslate**](gltranslate.md)e [**glScale**](glscale.md), anziché comporre matrici di rotazione, traduzione e scalabilità personalizzate e chiamare [**glMultMatrix**](glmultmatrix.md).
-   Usare [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) per salvare e ripristinare i valori di stato. Usare le funzioni di query solo quando l'applicazione richiede i valori di stato per i propri calcoli.
-   Usare gli elenchi di visualizzazione per incapsulare potenziali modifiche di stato con utilizzo intensivo di memoria. Inserire, ad esempio, tutte le chiamate [**glTexImage**](glteximage1d.md) necessarie per specificare completamente una trama (ed eventualmente anche le chiamate [**glTexParameter**](gltexparameter-functions.md), [**glPixelStore**](glpixelstore-functions.md)e [**glPixelTransfer**](glpixeltransfer.md) associate) in un unico elenco di visualizzazione. Chiamare questo elenco di visualizzazione per selezionare la trama.
-   Utilizzare gli elenchi di visualizzazione per incapsulare le chiamate di rendering di oggetti rigidi che verranno disegnati ripetutamente.
-   Per ridurre al minimo la larghezza di banda di rete in ambienti client/server, usare gli analizzatori anche per tassellature di superficie semplici.
-   Se possibile, per evitare il sovraccarico della \_ normalizzazione GL, fornire normali a lunghezza di unità. Poiché [**glScale**](glscale.md) richiede quasi sempre l'abilitazione \_ di GL Normalize, evitare di usare **glScale** durante l'illuminazione.
-   Se non è necessario l'ombreggiatura uniforme, impostare [**glShadeModel**](glshademodel.md) su GL \_ flat.
-   Usare una singola chiamata [**glClear**](glclear.md) per frame, se possibile. Non usare **glClear** per cancellare le piccole sottoaree dei buffer; utilizzarlo solo per cancellare completamente o quasi completamente il buffer.
-   Per creare più triangoli indipendenti, usare una singola chiamata anziché più chiamate a [**glBegin**](glbegin.md) ( \_ triangoli GL) o una chiamata a **glBegin** ( \_ poligono GL). Analogamente

    Per creare un singolo triangolo, usare \_ triangoli GL anziché \_ poligono GL.

    Usare una singola chiamata a [**glBegin**](glbegin.md) (GL \_ quad) invece di chiamare **glBegin** (GL \_ Polygon) ripetutamente.

    Usare una singola chiamata a [**glBegin**](glbegin.md) ( \_ linee GL) per creare più segmenti di linea indipendenti, anziché chiamare più volte **glBegin** (GL \_ Lines).

-   In generale, usare le forme vettoriali dei comandi per passare i dati pre-calcolati e usare le forme scalari dei comandi per passare i valori calcolati in prossimità del tempo di chiamata.
-   Evitare di apportare modifiche alla modalità ridondante, ad esempio impostando il colore sullo stesso valore tra i vertici di un poligono ombreggiato.
-   Quando si disegnano o si copiano immagini, si disabilitano le operazioni di rasterizzazione e di frammentazione per ottimizzare le risorse. OpenGL può applicare trame alle immagini pixel.

 

 




