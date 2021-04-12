---
title: Suggerimenti sulla correttezza OpenGL
description: Suggerimenti sulla correttezza OpenGL
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, suggerimenti per la correttezza
- OpenGL, procedure consigliate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5294d2e989591216ea8cf66aa380933718776f2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395707"
---
# <a name="opengl-correctness-tips"></a>Suggerimenti sulla correttezza OpenGL

Seguire queste linee guida per creare applicazioni OpenGL che svolgono le proprie esigenze:

-   Si supponga che il comportamento degli errori nella parte di un'implementazione di OpenGL possa cambiare in una versione futura di OpenGL. La semantica degli errori OpenGL può cambiare nelle future revisioni.
-   Usare la matrice di proiezione per comprimere tutta la geometria in un singolo piano. Se viene usata la matrice Modelview, le funzionalità OpenGL che operano in coordinate oculari, ad esempio l'illuminazione e i piani di ritaglio definiti dall'applicazione, potrebbero non riuscire.
-   Non apportare modifiche estese a una sola matrice. Ad esempio, non animare una rotazione chiamando continuamente [**glRotate**](glrotate.md) con un angolo incrementale. Usare invece [**glLoadIdentity**](glloadidentity.md) per inizializzare la matrice specificata per ogni fotogramma, quindi chiamare **glRotate** con l'angolo completo desiderato per il frame.
-   Si prevede che più passaggi attraverso un database di rendering generino gli stessi frammenti di pixel solo se questo comportamento è garantito dalle regole di invarianza stabilite per un'implementazione di OpenGL conforme. In caso contrario, più passaggi potrebbero generare set diversi di frammenti.
-   Non prevedere errori di segnalazione durante la definizione di un elenco di visualizzazione. I comandi all'interno di un elenco di visualizzazione generano errori solo quando l'elenco viene eseguito.
-   Per ottimizzare l'operazione del buffer di profondità, posizionare il piano Near tronco più lontano possibile dal punto di vista.
-   Chiamare [**glFlush**](glflush.md) per forzare l'esecuzione di tutti i comandi OpenGL precedenti. Non contare su [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o [**glIsEnabled**](glisenabled.md) per scaricare il flusso di rendering. I comandi di query scaricano la maggior parte del flusso necessario per restituire dati validi, ma non necessariamente completano tutti i comandi di rendering in sospeso.
-   Disabilitare la rethering durante il rendering delle immagini predette, ad esempio quando viene chiamato [**glCopyPixels**](glcopypixels.md) .
-   Utilizzare l'intera gamma del buffer di accumulo. Se ad esempio si accumulano quattro immagini, ridimensionarle in base a un trimestre mentre viene accumulato.
-   Per ottenere la rasterizzazione bidimensionale esatta, specificare attentamente sia la proiezione ortogonale che i vertici delle primitive da rasterizzare. Specificare la proiezione ortogonale con coordinate integer, come illustrato nell'esempio seguente.

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    La *larghezza* e l' *altezza* dei parametri sono le dimensioni del viewport. Data questa matrice di proiezione, posizionare i vertici del poligono e le posizioni delle immagini pixel in corrispondenza delle coordinate integer per la rasterizzazione prevedibile. Ad esempio, [glRecti](glrect-functions.md)(0, 0, 1, 1) riempie in modo affidabile il pixel inferiore sinistro del viewport e [glRasterPos2i](glrasterpos-functions.md)(0, 0) posiziona in modo affidabile un'immagine ingrandita sul pixel inferiore sinistro del viewport. Tuttavia, i vertici di punti, i vertici di riga e le posizioni bitmap devono essere posizionati in posizioni a metà Integer. Ad esempio, una linea disegnata da (*x* (1), 0,5) a (*x* (2), 0,5) verrà sottoposta a rendering in modo affidabile lungo la riga inferiore dei pixel nel viewport e un punto disegnato in (0,5, 0,5) verrà riempito in modo affidabile lo stesso pixel di glRecti (0, 0, 1, 1).

    Un compromesso ottimale che consente di specificare tutte le primitive in posizioni Integer, garantendo comunque la rasterizzazione prevedibile, consiste nel tradurre *x* e *y* di 0,375, come illustrato nell'esempio di codice seguente. Tale conversione mantiene i bordi delle immagini poligonali e pixel in modo sicuro dai centri dei pixel, mentre i vertici di linea vengono spostati abbastanza vicino ai pixel Center.

    ``` syntax
    glViewport(0, 0, width, height);
    glMatrixMode(GL_PROJECTION);
    glLoadIdentity( );
    gluOrtho2D(0, width, 0, height);
    glMatrixMode(GL_MODELVIEW);
    glLoadIdentity( );
    glTranslatef(0.375, 0.375, 0.0);
    /* render all primitives at integer positions */
    ```

-   Evitare di usare le coordinate del vertice con *l* negativo e le coordinate di trama *q* negative. OpenGL potrebbe non ritagliare correttamente le coordinate e può creare errori di interpolazione durante l'ombreggiatura delle primitive definite da tali coordinate.

 

 




