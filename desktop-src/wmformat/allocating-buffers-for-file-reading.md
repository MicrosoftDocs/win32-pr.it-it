---
title: Allocazione di buffer per la lettura di file
description: Allocazione di buffer per la lettura di file
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media Format SDK, lettura di file ASF
- Formato di sistemi avanzati (ASF), lettura di file
- ASF (Advanced Systems Format), lettura di file
- Windows Media Format SDK, allocazione di buffer
- ASF (Advanced Systems Format), allocazione di buffer
- ASF (formato avanzato dei sistemi), allocazione di buffer
- ASF (Advanced Systems Format), allocazione di buffer
- ASF (formato avanzato dei sistemi), allocazione di buffer
- allocazione di buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398536"
---
# <a name="allocating-buffers-for-file-reading"></a>Allocazione di buffer per la lettura di file

Nello scenario di lettura dei file più semplice, i buffer utilizzati per recapitare gli esempi vengono allocati dall'oggetto di lettura (l'oggetto Reader o l'oggetto Reader sincrono). È tuttavia possibile allocare i buffer manualmente. Per ulteriori informazioni sui vantaggi dell'allocazione di buffer personalizzati, vedere Supporto di [esempio allocato dall'utente](user-allocated-sample-support.md).

Per usare i propri buffer per la lettura dei file, seguire questa procedura.

1.  Implementare un callback o callback per il lettore da chiamare quando è necessario un buffer. Se si leggono esempi di output, usare [**IWMReaderAllocatorEx:: AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex). Se si leggono esempi di flusso, usare [**IWMReaderAllocatorEx:: AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex). Includere qualsiasi logica per la gestione dei buffer più adatti all'applicazione.
2.  Allocare un pool di buffer che si utilizzerà per la lettura dei file.
    -   Trovare le dimensioni necessarie per i buffer chiamando [**IWMReaderAdvanced:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) o [**IWMReaderAdvanced:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) per ogni output e/o flusso per il quale viene usato il buffer. Se si usa il lettore sincrono, usare invece [**IWMSyncReader:: GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) o [**IWMSyncReader:: GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) .
    -   Creare ogni buffer per il pool.
3.  Configurare il Reader o il lettore sincrono per la lettura. Per ulteriori informazioni, vedere la pagina relativa alla [lettura di file con il Reader asincrono](reading-files-with-the-asynchronous-reader.md) o la [lettura di file con il lettore sincrono](reading-files-with-the-synchronous-reader.md).
4.  Prima di iniziare la scrittura, chiamare [**IWMReaderAdvanced:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) o [**IWMReaderAdvanced:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) per ogni output e flusso per il quale si stanno allocando buffer utilizzando l'oggetto Reader. Per il lettore sincrono, chiamare [**IWMSyncReader2:: SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) o [**IWMSyncReader2:: SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) .
5.  Iniziare a leggere il file.

L'oggetto di lettura effettuerà chiamate al callback allocatore appropriato e otterrà esempi dall'applicazione. La logica di gestione del buffer deve includere un modo per segnalare che un buffer può essere usato di nuovo. In genere, quando viene eseguito il rendering del relativo contenuto, un buffer viene inserito nuovamente nel pool. A seconda dell'applicazione, potrebbero essere necessari solo pochi buffer nel pool o in molti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Lettura di file ASF**](reading-asf-files.md)
</dt> </dl>

 

 




