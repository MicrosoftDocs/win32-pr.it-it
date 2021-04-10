---
title: Scrittura di file ASF
description: Scrittura di file ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media Format SDK, scrittura di file ASF
- Windows Media Format SDK, creazione di file ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Formato di sistemi avanzati (ASF), scrittura di file
- ASF (Advanced Systems Format), scrittura di file
- ASF (Advanced Systems Format), creazione di file
- ASF (Advanced Systems Format), creazione di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858006"
---
# <a name="writing-asf-files"></a>Scrittura di file ASF

È possibile utilizzare l'oggetto writer di Windows Media Format SDK per creare file ASF da dati multimediali digitali. Per creare un'istanza dell'oggetto writer, chiamare la funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . L'oggetto writer coordina la funzionalità di un numero di componenti, inclusi i codec, che sono esterni a Windows Media Format SDK.

La funzionalità di base dell'oggetto writer può essere suddivisa nei passaggi seguenti. In questa procedura, "l'applicazione" si riferisce al programma scritto utilizzando Windows Media Format SDK.

1.  L'applicazione fornisce al writer un profilo da utilizzare per la creazione del file ASF. Quando il writer carica i dati del profilo, assegna un numero di input a ogni connessione del profilo.
2.  L'applicazione fornisce al writer il nome di un file di output per il file da scrivere. Il writer crea un oggetto sink di file del writer per gestire la creazione e l'input del file. Per altre informazioni, vedere [oggetto sink di file writer](writer-file-sink-object.md).
3.  Il writer crea un'intestazione per il nuovo file in base alle informazioni contenute nel profilo.
4.  L'applicazione passa campioni non compressi al writer. Gli esempi vengono passati uno alla volta nei buffer racchiusi tra oggetti buffer. L'applicazione deve passare esempi per ogni flusso in modo simultaneo, in modo che il writer riceva tutti gli esempi in ordine di tempo di presentazione.
5.  Il writer passa gli esempi al codec appropriato per la compressione. Quando il writer riceve gli esempi compressi, li invia con esempi dagli altri flussi, in modo che i campioni vengano inseriti nel file in base all'ordine dei tempi di presentazione indipendentemente dal flusso. I dati di esempio vengono quindi creati in pacchetti e scritti nella sezione dati del file.
6.  Quando vengono elaborati tutti gli esempi, il writer può aggiungere un indice al file per migliorare le prestazioni di ricerca.

Questi passaggi sono illustrati nell'applicazione di esempio WMStats, tra gli altri. Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).

Il writer supporta inoltre funzionalità più avanzate che consentono di eseguire le operazioni seguenti:

-   Modificare i metadati nell'intestazione del file.
-   Scrivere esempi precompressi.
-   Scrivere in sink di rete per lo streaming di dati in tempo reale.
-   Scrivi nei sink di file per le opzioni avanzate di controllo file.
-   Scrivere nei sink di push per la distribuzione nei server che forniranno contenuto agli utenti finali.
-   Fornire esempi di PostView per la verifica dell'output.
-   Recapitare le statistiche sulle prestazioni del writer.

Nelle sezioni seguenti viene descritto in dettaglio l'utilizzo dell'oggetto writer.



| Sezione                                                                    | Descrizione                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Per utilizzare profili con il writer](to-use-profiles-with-the-writer.md)     | Viene descritto come specificare un profilo da utilizzare con il writer.                                             |
| [Utilizzo degli input](working-with-inputs.md)                             | Viene descritto come identificare e configurare le impostazioni di input nel writer.                              |
| [Per modificare i metadati con il writer](to-edit-metadata-with-the-writer.md)   | Viene descritto come utilizzare il writer per modificare i metadati per un nuovo file.                                       |
| [Per scrivere esempi](to-write-samples.md)                                   | Viene descritto come passare campioni al writer.                                                           |
| [Impostazione delle estensioni delle unità dati](setting-data-unit-extensions.md)           | Viene descritto come aggiungere dati estesi ad esempi.                                                         |
| [Scrittura di esempi compressi](writing-compressed-samples.md)               | Viene descritto come passare gli esempi pre-compressi al writer.                                            |
| [Scrittura di flussi di immagini](writing-image-streams.md)                         | Viene descritto come configurare un input per un flusso di immagini.                                               |
| [Creazione di esempi di immagini video](writing-video-image-samples.md)             | Viene descritto come configurare esempi di immagini video.                                                        |
| [Scrittura di flussi di velocità in bit variabili](writing-variable-bit-rate-streams.md) | Viene descritto come scrivere flussi di velocità in bit variabile (VBR).                                                |
| [Uso della codifica Two-Pass](using-two-pass-encoding.md)                     | Viene descritto come fare in modo che il codec esegua un passaggio preliminare prima di scrivere il file.                    |
| [Per forzare l'inserimento di Key-Frame](to-force-key-frame-insertion.md)           | Viene descritto come forzare manualmente il codec a codificare un campione come fotogramma chiave.                           |
| [Per gestire la latenza del writer](to-manage-writer-latency.md)                   | Viene descritto come ridurre al minimo il tempo impiegato dal writer per elaborare gli esempi in un file o un sink di output. |
| [Utilizzo dei sink di writer](working-with-writer-sinks.md)                 | Viene descritto come usare i sink del writer per distribuire il contenuto a file o percorsi di rete.               |
| [Per ottenere le statistiche del writer](to-get-writer-statistics.md)                   | Viene descritto come ottenere le statistiche per il writer.                                                        |
| [Per utilizzare PostView writer](to-use-writer-postview.md)                       | Viene descritto come ottenere campioni non compressi durante la scrittura di un file per la verifica.                        |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> <dt>

[**Oggetto file sink del writer**](writer-file-sink-object.md)
</dt> <dt>

[**Oggetto sink di rete writer**](writer-network-sink-object.md)
</dt> <dt>

[**Oggetto writer**](writer-object.md)
</dt> </dl>

 

 




