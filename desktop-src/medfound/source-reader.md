---
description: Il lettore di origine rappresenta un'alternativa all'uso della sessione multimediale e della pipeline Microsoft Media Foundation per elaborare i dati multimediali.
ms.assetid: 8a17a754-53ef-4c05-9189-7978d864b17a
title: Lettore di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ba67b32fba7fcf899f339e9e2d0512d2574bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527829"
---
# <a name="source-reader"></a>Lettore di origine

Il lettore di origine rappresenta un'alternativa all'uso della [sessione multimediale](media-session.md) e della pipeline Microsoft Media Foundation per elaborare i dati multimediali.

## <a name="why-use-the-source-reader"></a>Perché usare il lettore di origine?

Media Foundation fornisce una pipeline ottimizzata per la riproduzione. La pipeline è end-to-end, ovvero gestisce il flusso di dati dall'origine, ad esempio un file video, fino alla destinazione, ad esempio la visualizzazione grafica. Tuttavia, se si desidera leggere o modificare i dati durante la pipeline, è necessario scrivere un plug-in personalizzato. Questa operazione richiede una conoscenza abbastanza approfondita della pipeline Media Foundation. Per alcune attività, la creazione di un nuovo plug-in è un sovraccarico eccessivo. Il lettore di origine è progettato per questo tipo di situazione, quando si desidera ottenere i dati non elaborati da un'origine senza l'overhead dell'intera pipeline.

Internamente, il lettore di origine include un puntatore a un'origine multimediale. Un' *origine multimediale* è un oggetto Media Foundation che genera dati multimediali da un'origine esterna, ad esempio un file multimediale o un dispositivo di acquisizione video. Il lettore di origine gestisce tutte le chiamate al metodo all'origine multimediale. Per altre informazioni sulle origini multimediali, vedere [origini multimediali](media-sources.md).

Se l'origine multimediale recapita dati compressi, è possibile usare il lettore di origine per decodificare i dati. In tal caso, il lettore di origine caricherà il decoder corretto e gestirà il flusso di dati tra l'origine multimediale e il decodificatore. Il lettore di origine può anche eseguire un'elaborazione video limitata: conversione dei colori da YUV a RGB-32 e deinterlacciamento software, anche se queste operazioni non sono consigliate per il rendering video in tempo reale. Questo processo è illustrato nella figura seguente.

![diagramma del lettore di origine](images/sourcereader.png)

Il lettore di origine non invia i dati a una destinazione. è necessario che l'applicazione utilizzi i dati. Ad esempio, il lettore di origine può leggere un file video, ma non eseguirà il rendering del video sullo schermo. Inoltre, il lettore di origine non gestisce un clock di presentazione, gestisce problemi di temporizzazione o Sincronizza video con audio.

Provare a usare il lettore di origine nei casi seguenti:

-   Si desidera ottenere dati da un file multimediale senza preoccuparsi della struttura di file sottostante.
-   Si desidera ottenere dati da un dispositivo di acquisizione audio o video.
-   Le attività di elaborazione dati non sono sensibili al tempo oppure non è necessario un clock di presentazione.
-   Si dispone già di una pipeline multimediale che non si basa su Media Foundation e si desidera incorporare i Media Foundation origini multimediali nella propria pipeline.

Il lettore di origine non è consigliato nelle situazioni seguenti:

-   Per il contenuto protetto. Il lettore di origine non supporta Digital Rights Management (DRM).
-   Se si è interessati ai dettagli della struttura di file sottostante. Il lettore di origine nasconde quel tipo di dettaglio.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                        | Descrizione                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Utilizzo del lettore di origine per l'elaborazione dei dati multimediali](processing-media-data-with-the-source-reader.md)<br/> | In questo argomento viene descritto come utilizzare il lettore di origine per elaborare i dati multimediali.<br/>                                               |
| [Utilizzo del lettore di origine in modalità asincrona](using-the-source-reader-in-asynchronous-mode.md)<br/>  | In questo argomento viene descritto come utilizzare il lettore di origine in modalità asincrona.<br/>                                                |
| [Esercitazione: decodifica audio](tutorial--decoding-audio.md)<br/>                                          | Questa esercitazione illustra come usare il lettore di origine per decodificare l'audio da un file multimediale e scrivere l'audio in un file WAVE.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Architettura di Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Guida alla programmazione di Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




