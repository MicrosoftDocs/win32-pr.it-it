---
description: Combinazione di acquisizione video e anteprima
ms.assetid: bffc1900-be05-4d7e-ab8d-3177365aeb7a
title: Combinazione di acquisizione video e anteprima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c1894e9431cbfa9e7bbbd0ef0bcec48021055350030b54ffd2f3e2729db81c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084327"
---
# <a name="combining-video-capture-and-preview"></a>Combinazione di acquisizione video e anteprima

Le sezioni precedenti descrivono come acquisire video in vari formati di file. La sezione [Video di anteprima](previewing-video.md) descrive come creare un grafico di anteprima live. Tuttavia, molte applicazioni devono eseguire entrambe le operazioni contemporaneamente. Per creare un grafico combinato di anteprima e scrittura di file, è sufficiente effettuare due chiamate a [**ICaptureGraphBuilder2::RenderStream:**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)


```C++
// Render the preview stream to the video renderer.
hr = pBuild->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Video, pCap, 
    NULL, NULL);

// Render the capture stream to the mux.
hr = pBuild->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Video, pCap, 
    NULL, pMux);
```



In questo codice, Capture Graph Builder nasconde alcuni dettagli:

-   Se il filtro di acquisizione ha un pin di anteprima o un pin della porta video, oltre a un pin di acquisizione, il metodo [**RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) esegue semplicemente il rendering di entrambi i pin, come illustrato nella figura seguente.

    ![Grafico di acquisizione e anteprima](images/vidcap04.png)

-   Se il filtro ha solo un pin di acquisizione, Capture Graph Builder usa il filtro [Smart Tee](smart-tee-filter.md) per suddividere il flusso di acquisizione. La figura seguente mostra il grafico con smart tee.

    ![Grafico di acquisizione e anteprima con filtro Smart Tee](images/vidcap05.png)

Il filtro Smart Tee include un pin di acquisizione e un pin di anteprima. Accetta un singolo flusso video dal filtro di acquisizione e lo suddivide in due flussi, uno per l'acquisizione e uno per l'anteprima. Per mantenere la velocità effettiva sul pin di acquisizione, il pin di anteprima elimina i fotogrammi in base alle esigenze. Rimuove inoltre i timestamp da ogni esempio prima di recapitarlo, per i motivi descritti nell'argomento DirectShow [filtri di acquisizione video.](directshow-video-capture-filters.md)

Anche se smart tee suddivide il flusso, non duplica fisicamente i dati video. Usa invece oggetti di esempio multimediali personalizzati che condividono i buffer. Gli esempi sono contrassegnati come "di sola lettura" per garantire che i filtri downstream non scrivono sui dati.

Se il grafico di acquisizione ha una finestra di anteprima, diversi elementi possono causare l'arresto dell'intero grafico da parte di Filter Graph Manager, incluso il flusso di acquisizione:

-   Blocco del computer.
-   Premere CTRL+ALT+CANC in un computer membro di un dominio.
-   Esecuzione di un'applicazione Direct3D a schermo intero, ad esempio un gioco o un screen saver.
-   Cambio di monitor o modifica della risoluzione dello schermo.
-   Esecuzione di un programma che Windows visualizzare una finestra di dialogo Controllo dell'account utente. (Windows Vista o versione successiva.
-   Esecuzione di una finestra DOS a schermo intero.

Uno di questi eventi potrebbe interrompere la sessione di acquisizione, causando eventualmente la perdita di dati. Ecco cosa accade internamente: il renderer video perde le risorse Direct3D o DirectDraw necessarie. Durante il ripristino di tali risorse, il renderer video deve riconnettersi al filtro upstream, causando l'arresto del grafo da parte di Filter Graph Manager.

Di seguito sono riportate due possibili soluzioni a questo problema:

-   Non includere un flusso di anteprima. Tenere tuttavia presente che il [**metodo ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) aggiunge automaticamente una finestra di anteprima quando il dispositivo di acquisizione ha un pin della porta video. Vedere [Pin della porta video in Acquisizione file.](video-port-pins-in-file-capture.md)
-   Usare il motore di buffer di flusso per inviare il flusso di anteprima a un grafo in un altro processo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione di video in un file](capturing-video-to-a-file.md)
</dt> </dl>

 

 



