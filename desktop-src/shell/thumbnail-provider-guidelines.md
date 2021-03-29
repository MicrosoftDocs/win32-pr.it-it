---
description: Quando si fornisce un'anteprima, è necessario seguire le linee guida riportate di seguito.
title: Linee guida per gestore anteprime
ms.topic: article
ms.date: 05/31/2018
ms.assetid: a1d29992-1347-4574-81b9-b90e2b0938f1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 062c363b4faea9fd07888a55e2dd3896b138c599
ms.sourcegitcommit: 9763c9cb859df3530766b6e65f9dce4f7de87fd2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/11/2020
ms.locfileid: "104118690"
---
# <a name="thumbnail-handler-guidelines"></a>Linee guida per gestore anteprime

Quando si fornisce un'anteprima, è necessario seguire le linee guida riportate di seguito.

-   Fornire anteprime che vengono visualizzate correttamente in una risoluzione di 256x256 pixel in un colore a 32 bit. Un'anteprima di questa dimensione viene utilizzata dal riquadro di lettura di Windows Vista in assenza di un gestore di anteprime registrato. Tuttavia, un gestore di anteprime è l'opzione consigliata e deve essere fornita laddove possibile.
-   Quando si creano più immagini con dimensioni diverse, non creare le immagini più piccole dal più grande ritagliare la pagina, il frame o l'immagine. Ridimensionare l'intera immagine.
-   Non visualizzare più pagine, frame o immagini contemporaneamente; è sufficiente utilizzarne uno. Se un documento è costituito da più pagine, ad esempio un documento di testo o un foglio di calcolo costituito da più fogli di lavoro, la pagina di copertina è spesso la scelta migliore, ma indipendentemente da quella usata, ne viene usata solo una. Non aggregare pagine diverse, che offrono un aspetto confuso.
-   Windows Vista è responsabile della scalabilità verticale o verticale delle immagini di campionamento. Se al gestore viene richiesta un'immagine più grande di quella disponibile, fornire le dimensioni più vicine. Non tentare di ridimensionare in modo dinamico la propria immagine.
-   Restituire sempre un'immagine di anteprima dal gestore anziché eseguire una logica speciale per restituire icone tradizionali. Al di sotto di una determinata dimensione, Windows Vista Visualizza automaticamente un'icona tradizionale al posto dell'anteprima. Per altri dettagli, vedere la sezione relativa alla *cache e al ridimensionamento delle anteprime* dei [gestori di anteprime](thumbnail-providers.md) .
-   Restituisce sempre un'anteprima con le proporzioni della pagina, del frame o dell'immagine. Non usare Alpha per completare un quadrato. Windows Vista è responsabile del corretto posizionamento di un'immagine non quadrata.
-   Non aggiungere aree di visualizzazione alle anteprime. Quando appropriato, Windows Vista applica automaticamente le ombreggiature e altre aree di riscontro. Applica anche aree di modifica speciali per determinati tipi di file, ad esempio immagini o video.
-   Non sovrapporre il tipo di file o le informazioni sull'applicazione nell'anteprima. In Windows Vista viene visualizzata una sovrapposizione dei tipi nell'angolo inferiore destro dell'immagine. Questa sovrapposizione è basata sul tipo percepito, ma può essere impostata per singoli tipi di file.
-   Per ottenere prestazioni ottimali, quando l'anteprima è basata sul contenuto di un file, ad esempio una pagina di un documento, archiviare l'immagine di anteprima quando il file viene salvato (e quindi probabilmente modificato) anziché calcolarlo in tempo reale. Questa operazione deve essere eseguita se il calcolo è a elevato utilizzo di memoria (più di uno o due secondi). Se questa operazione non viene eseguita, le visualizzazioni che mostrano un numero elevato di file le cui anteprime sono gestite da diversi gestori determineranno un po' di tempo per la visualizzazione, un'esperienza utente non valida. Windows Vista memorizza le anteprime e fa riferimento all'ora dell'Ultima modifica per determinare se è necessario aggiornare un'anteprima.
-   Tenere presente che Explorer può scegliere di non visualizzare un'anteprima anche se è disponibile un provider. Ad esempio, un file archiviato su nastro non verrà richiamato per ottenere l'anteprima.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestori di anteprime](thumbnail-providers.md)
</dt> <dt>

[Compilazione di gestori di anteprime](building-thumbnail-providers.md)
</dt> </dl>

 

 



