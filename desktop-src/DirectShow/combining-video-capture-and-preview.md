---
description: Combinazione di acquisizione video e anteprima
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinazione di acquisizione video e anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d1a3dd3df30bd13aa6fdae7e39894941071df8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481173"
---
# <a name="combining-video-capture-and-preview"></a>Combinazione di acquisizione video e anteprima

Le sezioni precedenti descrivono come acquisire video in vari formati di file. La sezione anteprima del [video](previewing-video.md) descrive come compilare un grafico di anteprima in tempo reale. Tuttavia, molte applicazioni devono eseguire entrambe contemporaneamente. Per compilare un grafo combinato di anteprima e di scrittura di file, è sufficiente effettuare due chiamate a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream):


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



In questo codice, il generatore di grafici di acquisizione nasconde alcuni dettagli:

-   Se il filtro di acquisizione include un pin di anteprima o un PIN della porta video, più un pin di acquisizione, il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) esegue semplicemente il rendering di entrambi i pin, come illustrato nella figura seguente.

    ![Acquisisci e visualizza l'anteprima del grafico](images/vidcap04.png)

-   Se il filtro ha solo un pin di acquisizione, il generatore del grafico di acquisizione usa il filtro [Smart Tee](smart-tee-filter.md) per suddividere il flusso di acquisizione. La figura seguente mostra il grafico con una Smart Tee.

    ![Acquisisci e visualizza in anteprima il grafico con filtro Smart Tee](images/vidcap05.png)

Il filtro Smart Tee include un pin di acquisizione e un pin di anteprima. Accetta un solo flusso video dal filtro di acquisizione e lo suddivide in due flussi, uno per l'acquisizione e uno per l'anteprima. Per mantenere la velocità effettiva sul pin di acquisizione, il pin di anteprima Elimina i frame in base alle esigenze. Elimina inoltre i timestamp di ogni campione prima di distribuirlo, per i motivi illustrati nell'argomento [filtri di acquisizione video DirectShow](directshow-video-capture-filters.md).

Sebbene lo Smart Tee suddivida il flusso, non duplica fisicamente i dati del video. USA invece oggetti di esempio multimediali personalizzati che condividono i buffer. Gli esempi sono contrassegnati come "di sola lettura" per garantire che i filtri downstream non scrivano sui dati.

Se nel grafico di acquisizione è presente una finestra di anteprima, è possibile che Filter Graph Manager arresti l'intero grafico, incluso il flusso di acquisizione:

-   Blocco del computer.
-   Premere CTRL + ALT + CANC in un computer membro di un dominio.
-   Esecuzione di un'applicazione Direct3D a schermo intero, ad esempio un gioco o un screen saver.
-   Cambio di monitor o modifica della risoluzione dello schermo.
-   Esecuzione di un programma che fa in modo che Windows visualizzi una finestra di dialogo controllo dell'account utente (UAC). (Windows Vista o versioni successive).
-   Esecuzione di una finestra DOS a schermo intero.

Uno di questi eventi potrebbe interrompere la sessione di acquisizione, causando possibili perdite di dati. (Ecco cosa accade internamente: il renderer video perde le risorse Direct3D o DirectDraw necessarie. Durante il processo di recupero di tali risorse, il renderer video deve riconnettersi al filtro upstream, causando l'arresto del grafo da parte del gestore del grafico del filtro.

Di seguito sono riportate due possibili soluzioni a questo problema:

-   Non includere un flusso di anteprima. Tuttavia, tenere presente che il metodo [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) aggiunge automaticamente una finestra di anteprima quando il dispositivo di acquisizione ha un PIN della porta video. Vedere [pin della porta video nell'acquisizione di file](video-port-pins-in-file-capture.md).
-   Usare il motore di buffer del flusso per inviare il flusso di anteprima a un grafico in un altro processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



