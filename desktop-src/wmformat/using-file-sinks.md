---
title: Uso di file sink
description: Uso di file sink
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- ASF (Advanced Systems Format), sink di file
- ASF (formato avanzato dei sistemi), sink di file
- ASF (Advanced Systems Format), sink
- ASF (formato avanzato dei sistemi), sink
- sink, sink di file
- sink di file, informazioni
- sink di file, creazione
- sink di file, arresto
- sink di file, avvio
- sink di file, chiusura
- sink, statistiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104117454"
---
# <a name="using-file-sinks"></a>Uso di file sink

In circostanze normali, è possibile passare semplicemente il writer a un nome di file di output usando il metodo [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) e l'oggetto writer scriverà il file su disco automaticamente. In questo caso, il writer sta effettivamente creando e controllando un oggetto sink di file del writer che gestisce la scrittura del file su disco. Un oggetto sink di file writer controlla il flusso di dati dall'oggetto writer a un singolo file.

È possibile creare sink di file personalizzati per ottenere un maggiore controllo sulla modalità di scrittura del file da parte del sink. È anche possibile accedere al sink di file del writer predefinito creato dal writer in risposta a una chiamata a **SetOutputFilename**.

## <a name="creating-file-sinks"></a>Creazione di sink di file

Per creare un sink di file e aggiungerlo al writer, seguire questa procedura.

1.  Creare un nuovo sink chiamando la funzione [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) .
2.  Specificare un nome file per il sink chiamando [**IWMWriterFileSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).
3.  Aggiungere il sink di file al writer chiamando [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).
4.  Eseguire la scrittura nel modo consueto.
5.  Al termine della scrittura, il sink chiuderà automaticamente il file.

## <a name="stopping-and-starting-file-sinks"></a>Arresto e avvio di sink di file

Dopo l'inizio delle operazioni di scrittura, è possibile arrestare la scrittura in un sink di file chiamando [**IWMWriterFileSink2:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).

Esistono molti possibili motivi per cui si vuole interrompere la scrittura in un sink. Ad esempio, se si esegue la registrazione da un'origine live, è possibile che si sia interessati solo ad alcuni contenuti.

È possibile riprendere la scrittura in un sink di file chiamando [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start). Sia l' **arresto** che l' **avvio** usano i tempi di presentazione per controllare approssimativamente quando viene eseguito il comando. È possibile utilizzare i metodi [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) per ottenere un maggiore controllo sulle ore di inizio e di fine.

## <a name="closing-file-sinks"></a>Chiusura di sink di file

In genere, un sink di file viene chiuso automaticamente. Se la scrittura in un sink è stata completata, ma la scrittura di operazioni in altri sink continua, è necessario chiudere in modo esplicito il sink per conservare le risorse. Per chiudere un sink di file, chiamare [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).

## <a name="getting-sink-statistics"></a>Recupero delle statistiche del sink

È possibile ottenere le dimensioni e la durata del file per un sink aperto chiamando [**IWMWriterFileSink2:: Filesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) e [**IWMWriterFileSink2:: GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) rispettivamente.

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

 

 




