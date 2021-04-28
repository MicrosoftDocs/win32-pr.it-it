---
description: Uso del writer di sink
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Uso del writer di sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4fa472bd1a5121454b3ffb06def7082508432b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110489"
---
# <a name="using-the-sink-writer"></a>Uso del writer di sink

## <a name="overview"></a>Panoramica

### <a name="file-container-types"></a>Tipi di contenitore di file

Il writer di sink include il supporto predefinito per diversi tipi di contenitore di file. Per un elenco completo, vedere [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md). È possibile supportare tipi di contenitori aggiuntivi scrivendo un [sink multimediale personalizzato.](media-sinks.md) Il contenitore di file viene specificato quando si crea una nuova istanza del writer di sink.

### <a name="stream-formats"></a>Formati di flusso

Per ogni flusso, l'applicazione deve specificare quanto segue.

-   Il *formato di input* è il formato inviato dall'applicazione al writer di sink.
-   Il *formato di* output è il formato che verrà scritto nel file.

I formati di input e output possono essere compressi o non compressi. Il writer di sink supporta le combinazioni seguenti:

-   Input non compresso con output compresso. Questo è il caso tipico e viene usato per scenari di codifica o transcodico. Deve Microsoft Media Foundation disponibile un codificatore che accetta il tipo di input e codifica il tipo di output.
-   Input compresso con output identico. Usare questa combinazione per modificare la conversione di un file senza transcodico.
-   Input non compresso con output identico. Usare questa combinazione per scrivere audio o video non compressi in un contenitore di file.

Il writer sink non supporta il ridimensionamento video, la conversione della frequenza dei fotogrammi o il ricampionamento audio, a meno che queste funzioni non siano fornite dal codificatore. In caso contrario, l'applicazione può [usare processori](windowsmediadigitalsignalprocessors.md) di segnale digitale per convertire i dati di input, prima di inviare i dati al

## <a name="creating-the-sink-writer"></a>Creazione del writer di sink

Esistono due funzioni che creano il writer di sink:

-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) accetta l'URL di un file di output o un puntatore a un flusso di byte. Questa funzione crea internamente il sink multimediale.
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) accetta un puntatore a un sink multimediale già creato dall'applicazione.

Se si usa uno dei sink multimediali predefiniti, è preferibile usare la funzione [**MFCreateSinkWriterFromURL,**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) perché il chiamante non deve configurare il sink multimediale.

Il [**metodo MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) offre diverse opzioni per specificare il tipo di contenitore di file. Nel caso più semplice, la funzione usa l'estensione di file nell'URL per selezionare il contenitore di file. Per informazioni dettagliate, vedere la pagina di riferimento delle funzioni.

Ad esempio, il codice seguente specifica il nome file "output.wmv" per l'URL. In base all'estensione del nome file, il writer di sink carica il sink del supporto [ASF](asf-media-sinks.md) per creare un file ASF (Advanced Systems Format).


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



Nel caso di [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), il tipo di file è determinato dal sink multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sink Writer](sink-writer.md)
</dt> </dl>

 

 



