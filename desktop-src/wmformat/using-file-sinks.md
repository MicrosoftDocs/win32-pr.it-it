---
title: Uso di file sink
description: Uso di file sink
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Advanced Systems Format (ASF), sink di file
- ASF (Advanced Systems Format), sink di file
- Advanced Systems Format (ASF), sink
- ASF (Advanced Systems Format), sink
- sink, sink di file
- sink di file, informazioni
- sink di file, creazione
- sink di file, arresto
- sink di file, avvio
- sink di file, chiusura
- sink, statistiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f94bd6698ca30a645957da36cf3b81a84f9d3e7c8ce6c598be2c39f8ac766db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196174"
---
# <a name="using-file-sinks"></a>Uso di file sink

In circostanze normali, è sufficiente passare al writer un nome di file di output usando il metodo [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) e l'oggetto writer scriverà automaticamente il file su disco. In questo caso, il writer crea e controlla effettivamente un oggetto sink del file writer che gestisce la scrittura del file su disco. Un oggetto sink del file writer controlla il flusso di dati dall'oggetto writer a un singolo file.

È possibile creare sink di file personalizzati per ottenere un maggiore controllo sulla modalità di scrittura del file da parte del sink. È anche possibile accedere al sink del file writer predefinito creato dal writer in risposta a una chiamata a **SetOutputFilename**.

## <a name="creating-file-sinks"></a>Creazione di sink di file

Per creare un sink di file e aggiungerlo al writer, seguire questa procedura.

1.  Creare un nuovo sink chiamando la [**funzione WMCreateWriterFileSink.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
2.  Specificare un nome file per il sink chiamando [**IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).
3.  Aggiungere il sink di file al writer chiamando [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).
4.  Eseguire la scrittura nel modo consueto.
5.  Al termine della scrittura, il sink chiuderà automaticamente il file.

## <a name="stopping-and-starting-file-sinks"></a>Arresto e avvio di sink di file

Dopo l'inizio delle operazioni di scrittura, è possibile interrompere la scrittura in un sink di file chiamando [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).

Esistono molti potenziali motivi per cui è necessario interrompere la scrittura in un sink. Ad esempio, se si sta registrando da un'origine live, si potrebbe essere interessati solo ad alcuni contenuti.

È possibile riprendere la scrittura in un sink di file chiamando [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start). Sia **Arresta** che **Avvia usano** gli orari di presentazione per controllare approssimativamente quando viene eseguito il comando. È possibile usare i [**metodi IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) per ottenere un maggiore controllo sui tempi di avvio e arresto.

## <a name="closing-file-sinks"></a>Chiusura di sink di file

In genere, un sink di file viene chiuso automaticamente. Se la scrittura in un sink è terminata, ma le operazioni di scrittura in altri sink continuano, è necessario chiudere in modo esplicito il sink per conservare le risorse. Per chiudere un sink di file, chiamare [**IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).

## <a name="getting-sink-statistics"></a>Recupero delle statistiche del sink

È possibile ottenere le dimensioni e la durata del file per un sink aperto chiamando [**rispettivamente IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) e [**IWMWriterFileSink2::GetFileDuration.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**Interfaccia IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**Interfaccia IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**Oggetto file sink del writer**](writer-file-sink-object.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




