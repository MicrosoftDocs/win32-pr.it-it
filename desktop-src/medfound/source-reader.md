---
description: Il lettore di origine è un'alternativa all'uso della sessione multimediale e della pipeline Microsoft Media Foundation per elaborare i dati multimediali.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Lettore di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81527392c97aae039de8b8cdbd76b1251e03842b6b66c22cc224118d4f428620
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101815"
---
# <a name="source-reader"></a>Lettore di origine

Il lettore di origine è un'alternativa all'uso della [sessione multimediale](media-session.md) e della pipeline Microsoft Media Foundation per elaborare i dati multimediali.

## <a name="why-use-the-source-reader"></a>Perché usare il lettore di origine?

Media Foundation fornisce una pipeline ottimizzata per la riproduzione. La pipeline è end-to-end, ovvero gestisce il flusso di dati dall'origine (ad esempio un file video) fino alla destinazione (ad esempio la visualizzazione grafica). Tuttavia, se si vogliono leggere o modificare i dati mentre passano attraverso la pipeline, è necessario scrivere un plug-in personalizzato. Ciò richiede una conoscenza abbastanza approfondita della pipeline Media Foundation pipeline. Per determinate attività, la creazione di un nuovo plug-in è un sovraccarico troppo alto. Il lettore di origine è progettato per questo tipo di situazione, quando si vogliono ottenere i dati non elaborati da un'origine senza il sovraccarico dell'intera pipeline.

Internamente, il lettore di origine contiene un puntatore a un'origine multimediale. *Un'origine multimediale* è Media Foundation che genera dati multimediali da un'origine esterna, ad esempio un file multimediale o un dispositivo di acquisizione video. Il lettore di origine gestisce tutte le chiamate al metodo all'origine multimediale. Per altre informazioni sulle origini multimediali, vedere [Origini multimediali.](media-sources.md)

Se l'origine multimediale recapita dati compressi, è possibile usare il lettore di origine per decodificare i dati. In tal caso, il lettore di origine carica il decodificatore corretto e gestisce il flusso di dati tra l'origine multimediale e il decodificatore. Il lettore di origine può anche eseguire alcune operazioni di elaborazione video limitate: la conversione dei colori da YUV a RGB-32 e il dinterlacing software, anche se queste operazioni non sono consigliate per il rendering video in tempo reale. L'immagine seguente illustra questo processo.

![Diagramma del lettore di origine](images/sourcereader.png)

Il lettore di origine non invia i dati a una destinazione. è l'applicazione a usare i dati. Ad esempio, il lettore di origine può leggere un file video, ma non eseguirà il rendering del video sullo schermo. Inoltre, il lettore di origine non gestisce un orologio di presentazione, gestisce i problemi di temporizzazione o sincronizza i video con l'audio.

È consigliabile usare il lettore di origine quando:

-   Si vogliono ottenere dati da un file multimediale senza doversi preoccupare della struttura di file sottostante.
-   Si vogliono ottenere dati da un dispositivo di acquisizione audio o video.
-   Le attività di elaborazione dati non sono sensibili al tempo o non è necessario un orologio di presentazione.
-   Si dispone già di una pipeline multimediale che non è basata su Media Foundation e si vuole incorporare le origini multimediali Media Foundation nella propria pipeline.

Il lettore di origine non è consigliato nelle situazioni seguenti:

-   Per il contenuto protetto. Il lettore di origine non supporta DRM (Digital Rights Management).
-   Per informazioni dettagliate sulla struttura di file sottostante. Il lettore di origine nasconde il tipo di dettaglio.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                        | Descrizione                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Uso del lettore di origine per elaborare i dati multimediali](processing-media-data-with-the-source-reader.md)<br/> | In questo argomento viene descritto come utilizzare il lettore di origine per elaborare i dati multimediali.<br/>                                               |
| [Uso del lettore di origine in modalità asincrona](using-the-source-reader-in-asynchronous-mode.md)<br/>  | In questo argomento viene descritto come utilizzare il lettore di origine in modalità asincrona.<br/>                                                |
| [Esercitazione: Decodifica dell'audio](tutorial--decoding-audio.md)<br/>                                          | Questa esercitazione illustra come usare il lettore di origine per decodificare l'audio da un file multimediale e scriverlo in un file WAVE.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Media Foundation di programmazione](media-foundation-programming-guide.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




