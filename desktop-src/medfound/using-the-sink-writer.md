---
description: .
ms.assetid: BE89E2E0-711F-4BD5-BB86-AA4CCA2D3E7F
title: Uso del writer di sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46157eae6fe851468515f9d9653adb33918ebb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967119"
---
# <a name="using-the-sink-writer"></a>Uso del writer di sink

## <a name="overview"></a>Panoramica

### <a name="file-container-types"></a>Tipi di contenitori di file

Il writer di sink dispone del supporto incorporato per diversi tipi di contenitori di file. Per un elenco completo, vedere [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md). Per supportare tipi di contenitori aggiuntivi, è possibile scrivere un [sink multimediale](media-sinks.md)personalizzato. Il contenitore di file viene specificato quando si crea una nuova istanza del writer del sink.

### <a name="stream-formats"></a>Formati di flusso

Per ogni flusso, l'applicazione deve specificare quanto segue.

-   Il *formato di input* è il formato inviato dall'applicazione al writer del sink.
-   Il *formato di output* è il formato che verrà scritto nel file.

I formati di input e di output possono essere compressi o decompressi. Il writer di sink supporta le combinazioni seguenti:

-   Input non compresso con output compresso. Questo è il caso tipico e viene usato per gli scenari di codifica o di transcodifica. Deve essere disponibile un codificatore Microsoft Media Foundation che accetta il tipo di input e codifica per il tipo di output.
-   Input compresso con output identico. Usare questa combinazione per remux un file senza transcodifica.
-   Input non compresso con output identico. Usare questa combinazione per scrivere audio o video non compressi in un contenitore di file.

Il writer di sink non supporta il ridimensionamento video, la conversione della frequenza dei frame o il ricampionamento audio, a meno che queste funzioni non siano fornite dal codificatore. In caso contrario, l'applicazione può usare i [processori di segnale digitale](windowsmediadigitalsignalprocessors.md) per convertire i dati di input, prima di inviare i dati al

## <a name="creating-the-sink-writer"></a>Creazione del writer di sink

Sono disponibili due funzioni che creano il writer di sink:

-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) accetta l'URL di un file di output o un puntatore a un flusso di byte. Questa funzione crea il sink multimediale internamente.
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink) accetta un puntatore a un sink multimediale che è già stato creato dall'applicazione.

Se si usa uno dei sink di supporto incorporati, la funzione [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) è preferibile, perché il chiamante non deve configurare il sink multimediale.

Il metodo [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) fornisce diverse opzioni per specificare il tipo di contenitore di file. Nel caso più semplice, la funzione usa l'estensione del nome file nell'URL per selezionare il contenitore di file. Per informazioni dettagliate, vedere la pagina di riferimento per le funzioni.

Il codice seguente, ad esempio, specifica il nome file "output. wmv" per l'URL. In base all'estensione del nome di file, il writer di sink caricherà il [sink multimediale ASF](asf-media-sinks.md) per creare un file di formato Advanced Systems (ASF).


```C++
    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);
```



Nel caso di [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink), il tipo di file è determinato dal sink multimediale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Writer sink](sink-writer.md)
</dt> </dl>

 

 



