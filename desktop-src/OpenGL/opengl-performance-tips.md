---
title: OpenGL Performance Suggerimenti
description: OpenGL Performance Suggerimenti
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL, suggerimenti sulle prestazioni
- OpenGL, procedure consigliate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe91602d4a30767ed1e66e62d33445bf37152ede2cf9f8450e056f577cb3045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936831"
---
# <a name="opengl-performance-tips"></a>OpenGL Performance Suggerimenti

Queste procedure di programmazione ottimizzano le prestazioni dell'applicazione:

-   Usare [**glColorMaterial**](glcolormaterial.md) quando una sola proprietà materiale viene variata rapidamente ,ad esempio in ogni vertice. Usare [**glMaterial**](glmaterial-functions.md) per modifiche poco frequenti o quando più di una singola proprietà materiale viene variata rapidamente.
-   Usare [**glLoadIdentity per**](glloadidentity.md) inizializzare una matrice, anziché caricare una copia della matrice di identità.
-   Usare chiamate di matrice specifiche, ad esempio [**glRotate**](glrotate.md), [**glTranslate**](gltranslate.md)e [**glScale**](glscale.md), invece di comporre matrici di rotazione, traslazione e scala e [**chiamare glMultMatrix**](glmultmatrix.md).
-   Usare [**glPushAttrib e**](glpushattrib.md) [**glPopAttrib**](glpopattrib.md) per salvare e ripristinare i valori di stato. Usare le funzioni di query solo quando l'applicazione richiede i valori di stato per i propri calcoli.
-   Usare gli elenchi di visualizzazione per incapsulare le modifiche di stato potenzialmente a elevato utilizzo di memoria. Ad esempio, inserire tutte le chiamate [**glTexImage**](glteximage1d.md) necessarie per specificare completamente una trama (e forse anche le chiamate [**glTexParameter**](gltexparameter-functions.md), [**glPixelStore**](glpixelstore-functions.md)e [**glPixelTransfer**](glpixeltransfer.md) associate) in un singolo elenco di visualizzazione. Chiamare questo elenco di visualizzazione per selezionare la trama.
-   Usare gli elenchi di visualizzazione per incapsulare le chiamate di rendering di oggetti rigidi che verranno disegnati ripetutamente.
-   Per ridurre al minimo la larghezza di banda di rete negli ambienti client/server, usare gli analizzatori anche per semplici tessitori di superficie.
-   Se possibile, per evitare il sovraccarico di GL \_ NORMALIZE, specificare le normali a lunghezza unità. Poiché [**glScale richiede**](glscale.md) quasi sempre l'abilitazione di GL \_ NORMALIZE, evitare di **usare glScale quando** si esegue l'illuminazione.
-   Se l'ombreggiatura smussata non è necessaria, [**impostare glShadeModel**](glshademodel.md) su GL \_ FLAT.
-   Se possibile, usare una singola chiamata [**glClear**](glclear.md) per frame. Non usare **glClear** per cancellare piccole sottoaree dei buffer. usarlo solo per cancellare completamente o quasi completamente il buffer.
-   Per disegnare più triangoli indipendenti, usare una singola chiamata anziché più chiamate a [**glBegin**](glbegin.md) ( GL TRIANGLES ) o una chiamata \_ a **glBegin** ( GL \_ POLYGON ). Allo stesso modo:

    Per disegnare un singolo triangolo, usare GL \_ TRIANGLES anziché GL \_ POLYGON.

    Usare una singola chiamata a [**glBegin**](glbegin.md) ( GL QUADS ) anziché \_ chiamare ripetutamente **glBegin** ( GL \_ POLYGON).

    Usare una singola chiamata a [**glBegin**](glbegin.md) ( GL LINES ) per disegnare più segmenti di linea indipendenti, anziché \_ chiamare **glBegin** ( GL \_ LINES ) più volte.

-   In generale, usare le forme vettoriali dei comandi per passare i dati pre-calcolati e usare le forme scalari dei comandi per passare i valori calcolati in prossimità del tempo di chiamata.
-   Evitare di apportare modifiche alla modalità ridondante, ad esempio impostando il colore sullo stesso valore tra ogni vertice di un poligono con ombreggiatura piatta.
-   Quando si disegnano o si copiano immagini, disabilitare la rasterizzazione e le operazioni per frammento per ottimizzare le risorse. OpenGL può applicare trame alle immagini pixel.

 

 




