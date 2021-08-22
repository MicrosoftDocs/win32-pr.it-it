---
title: Scrittura di file ASF
description: Scrittura di file ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media Format SDK, scrittura di file ASF
- Windows Media Format SDK, creazione di file ASF
- Windows Media Format SDK,Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), scrittura di file
- ASF (Advanced Systems Format), scrittura di file
- Advanced Systems Format (ASF), creazione di file
- ASF (Advanced Systems Format), creazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4bec466a9f38dfedaa7e860fdc5e3eda56e0ca5fa1f1240bc18c54dfd51513
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590621"
---
# <a name="writing-asf-files"></a>Scrittura di file ASF

È possibile usare l'oggetto writer di Windows Media Format SDK per creare file ASF da dati multimediali digitali. Per creare un'istanza dell'oggetto writer, chiamare la [**funzione WMCreateWriter.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) L'oggetto writer coordina la funzionalità di diversi componenti, inclusi i codec, esterni all'SDK Windows Media Format.

La funzionalità di base dell'oggetto writer può essere suddivisa nei passaggi seguenti. In questa procedura, "l'applicazione" si riferisce al programma scritto usando Windows Media Format SDK.

1.  L'applicazione fornisce al writer un profilo da usare per la creazione del file ASF. Quando il writer carica i dati del profilo, assegna un numero di input a ogni connessione del profilo.
2.  L'applicazione fornisce al writer un nome di file di output per il file da scrivere. Il writer crea un oggetto sink del file writer per gestire la creazione e l'input del file. Per altre informazioni, vedere [Writer File Sink Object](writer-file-sink-object.md).
3.  Il writer crea un'intestazione per il nuovo file in base alle informazioni nel profilo.
4.  L'applicazione passa esempi non compressi al writer. Gli esempi vengono passati uno alla volta nei buffer di cui è stato eseguito il wrapping negli oggetti buffer. L'applicazione deve passare gli esempi per ogni flusso contemporaneamente in modo che il writer riceva tutti gli esempi in ordine di tempo di presentazione.
5.  Il writer passa gli esempi al codec appropriato per la compressione. Quando il writer riceve gli esempi compressi, li interfolia con gli esempi degli altri flussi in modo che gli esempi vadano nel file in ordine di tempo di presentazione indipendentemente dal flusso. I dati di esempio vengono quindi trasformati in pacchetti e scritti nella sezione dei dati del file.
6.  Quando vengono elaborati tutti gli esempi, il writer può aggiungere un indice al file per migliorare le prestazioni di ricerca.

Questi passaggi sono illustrati, tra gli altri, nell'applicazione di esempio WMStats. Per altre informazioni, vedere [Applicazioni di esempio.](sample-applications.md)

Lo scrittore supporta anche funzionalità più avanzate, consentendo di eseguire le operazioni seguenti:

-   Modificare i metadati nell'intestazione del file.
-   Scrivere esempi precompressi.
-   Scrivere nei sink di rete per lo streaming di dati live.
-   Scrivere nei sink di file per le opzioni avanzate di controllo dei file.
-   Scrivere nei sink push per la distribuzione nei server che consegneranno contenuto agli utenti finali.
-   Fornire esempi postview per la verifica dell'output.
-   Fornire statistiche sulle prestazioni del writer.

Le sezioni seguenti descrivono in dettaglio l'uso dell'oggetto writer.



| Sezione                                                                    | Descrizione                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Per utilizzare profili con il writer](to-use-profiles-with-the-writer.md)     | Viene descritto come specificare un profilo da utilizzare con il writer.                                             |
| [Uso degli input](working-with-inputs.md)                             | Viene descritto come identificare e configurare le impostazioni di input nel writer.                              |
| [Per modificare i metadati con il writer](to-edit-metadata-with-the-writer.md)   | Viene descritto come usare il writer per modificare i metadati per un nuovo file.                                       |
| [Per scrivere esempi](to-write-samples.md)                                   | Viene descritto come passare gli esempi al writer.                                                           |
| [Impostazione delle estensioni unità dati](setting-data-unit-extensions.md)           | Viene descritto come aggiungere dati estesi agli esempi.                                                         |
| [Scrittura di esempi compressi](writing-compressed-samples.md)               | Viene descritto come passare esempi precompressi al writer.                                            |
| [Scrittura di immagini Flussi](writing-image-streams.md)                         | Viene descritto come configurare un input per un flusso di immagine.                                               |
| [Scrittura di esempi di immagini video](writing-video-image-samples.md)             | Descrive come configurare gli esempi di immagini video.                                                        |
| [Scrittura di velocità in bit variabile Flussi](writing-variable-bit-rate-streams.md) | Viene descritto come scrivere flussi vbr (Variable Bit Rate).                                                |
| [Uso Two-Pass codifica](using-two-pass-encoding.md)                     | Viene descritto come fare in modo che il codec esere un passaggio preliminare prima di scrivere il file.                    |
| [Per forzare Key-Frame inserimento](to-force-key-frame-insertion.md)           | Viene descritto come forzare manualmente il codec per codificare un esempio come fotogramma chiave.                           |
| [Per gestire la latenza del writer](to-manage-writer-latency.md)                   | Viene descritto come ridurre al minimo il tempo necessario al writer per elaborare gli esempi in un file di output o in un sink. |
| [Uso dei sink del writer](working-with-writer-sinks.md)                 | Descrive come usare i sink del writer per recapitare il contenuto a file o percorsi di rete.               |
| [Per ottenere le statistiche del writer](to-get-writer-statistics.md)                   | Viene descritto come ottenere statistiche per il writer.                                                        |
| [Per usare Postview writer](to-use-writer-postview.md)                       | Viene descritto come ottenere esempi non compressi durante la scrittura di un file per la verifica.                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> <dt>

[**Oggetto file sink del writer**](writer-file-sink-object.md)
</dt> <dt>

[**Writer Network Sink Object**](writer-network-sink-object.md)
</dt> <dt>

[**Oggetto writer**](writer-object.md)
</dt> </dl>

 

 




