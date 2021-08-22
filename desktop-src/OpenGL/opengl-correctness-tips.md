---
title: OpenGL Correctness Suggerimenti
description: OpenGL Correctness Suggerimenti
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, suggerimenti per la correttezza
- OpenGL, procedure consigliate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588cb53ca9e096eb768c4ce448c0bb7badae6f01e7b8d7e16c31a631ebcafb47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486401"
---
# <a name="opengl-correctness-tips"></a>OpenGL Correctness Suggerimenti

Seguire queste linee guida per creare applicazioni OpenGL che funzionino come previsto:

-   Si supponga che il comportamento di errore da parte di un'implementazione OpenGL possa cambiare in una versione futura di OpenGL. La semantica degli errori OpenGL può cambiare nelle revisioni future.
-   Usare la matrice di proiezione per comprimere tutta la geometria in un singolo piano. Se si usa la matrice della visualizzazione modello, le funzionalità OpenGL che operano in coordinate oculare (ad esempio illuminazione e piani di ritaglio definiti dall'applicazione) potrebbero non riuscire.
-   Non apportare modifiche estese a una singola matrice. Ad esempio, non animare una rotazione chiamando continuamente [**glRotate**](glrotate.md) con un angolo incrementale. Usare invece [**glLoadIdentity**](glloadidentity.md) per inizializzare la matrice specificata per ogni frame e quindi chiamare **glRotate** con l'angolo completo desiderato per tale frame.
-   Prevedere più passaggi attraverso un database di rendering per generare gli stessi frammenti di pixel solo se questo comportamento è garantito dalle regole di invarianza stabilite per un'implementazione OpenGL conforme. In caso contrario, più passaggi potrebbero generare diversi set di frammenti.
-   Non prevedere che vengano segnalati errori durante la definizione di un elenco di visualizzazione. I comandi all'interno di un elenco di visualizzazione generano errori solo quando viene eseguito l'elenco.
-   Per ottimizzare il funzionamento del buffer di profondità, posizionare il piano del frustum vicino il più lontano possibile dal punto di vista.
-   Chiamare [**glFlush per**](glflush.md) forzare l'esecuzione di tutti i comandi OpenGL precedenti. Non contare su [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) o [**glIsEnabled**](glisenabled.md) per scaricare il flusso di rendering. I comandi di query scaricano tutta la parte del flusso necessaria per restituire dati validi, ma non completano necessariamente tutti i comandi di rendering in sospeso.
-   Disattivare il dithering durante il rendering di immagini predithering, ad esempio quando viene chiamato [**glCopyPixels.**](glcopypixels.md)
-   Usare l'intero intervallo del buffer di accumulo. Ad esempio, se si accumulano quattro immagini, ridimensionare ognuna di un quarto man appena viene accumulata.
-   Per ottenere la rasterizzazione bidimensionale esatta, specificare con attenzione sia la proiezione ortogonale che i vertici delle primitive da rasterizzare. Specificare la proiezione ortografica con coordinate intere, come illustrato nell'esempio seguente.

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    La larghezza e *l'altezza dei* parametri sono le dimensioni del viewport.  Data questa matrice di proiezione, posizionare i vertici poligoni e le posizioni delle immagini pixel in corrispondenza delle coordinate intere per rasterizzare in modo prevedibile. Ad esempio, [glRecti](glrect-functions.md)( 0, 0, 1, 1 ) riempie in modo affidabile il pixel inferiore sinistro del riquadro di visualizzazione e [glRasterPos2i](glrasterpos-functions.md)( 0, 0 ) posiziona in modo affidabile un'immagine non insonne in corrispondenza del pixel inferiore sinistro del viewport. Tuttavia, i vertici dei punti, i vertici delle linee e le posizioni delle bitmap devono essere posizionati in posizioni di semi-interi. Ad esempio, verrà eseguito il rendering affidabile di una linea disegnata da (*x* (1) , 0,5) a (*x* (2) , 0,5) lungo la riga inferiore di pixel nel viewport e un punto disegnato in corrispondenza di (0,5, 0,5) riempirà in modo affidabile lo stesso pixel di glRecti( 0, 0, 1, 1 ).

    Un compromesso ottimale che consente a tutte le primitive di essere specificate in posizioni integer, pur garantendo una rasterizzazione prevedibile, è la conversione *di x* e *y* di 0,375, come illustrato nell'esempio di codice seguente. Tale traslazione mantiene i bordi delle immagini di poligoni e pixel in modo sicuro dai centri dei pixel, spostando i vertici delle linee abbastanza vicini ai centri dei pixel.

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

-   Evitare di usare le *coordinate negative w* vertice e le coordinate di trama *q* negative. OpenGL potrebbe non ritagliare correttamente tali coordinate e può creare errori di interpolazione durante l'ombreggiatura delle primitive definite da tali coordinate.

 

 




