---
title: Per scrivere esempi
description: Per scrivere esempi
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- Advanced Systems Format (ASF), scrittura di esempi
- ASF (Advanced Systems Format), scrittura di esempi
- Advanced Systems Format (ASF), passando esempi al writer
- ASF (Advanced Systems Format), passando esempi al writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97907b2d313609f7f09dfc20e0c7f4f384c5328544ab75eb1516355edb6d318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653854"
---
# <a name="to-write-samples"></a>Per scrivere esempi

Dopo aver identificato e configurato gli input per il file che si sta scrivendo, è possibile iniziare a passare gli esempi al writer. È consigliabile passare gli esempi in ordine di tempo di presentazione, se possibile, per rendere più efficiente il processo di scrittura.

Prima di passare gli esempi, è necessario impostare il writer in modo che li accetti chiamando [**IWMWriter::BeginWriting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)

Per passare un esempio al writer, seguire questa procedura:

1.  Allocare un buffer e recuperare un puntatore [**all'interfaccia INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) chiamando [**IWMWriter::AllocateSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)
2.  Recuperare l'indirizzo del buffer creato nel passaggio 1 chiamando [**INSSBuffer::GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).
3.  Copiare i dati di esempio nella posizione del buffer, assicurando che l'esempio passato si adatti al buffer allocato. È possibile usare qualsiasi funzione di copia della memoria per copiare i dati. Una scelta comune è memcpy, inclusa nella libreria di runtime C standard.
4.  Aggiornare la quantità di dati usati nel buffer per riflettere le dimensioni effettive del campione chiamando [**INSSBuffer::SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Passare l'interfaccia del buffer al writer insieme al numero di input e all'ora di esempio usando il [**metodo IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) Tutti i campioni audio per un input rappresentano la stessa durata del contenuto, quindi è possibile calcolare il tempo di campionamento aggiungendo la durata del campione a un totale corrente. Per il video, è necessario calcolare il tempo in base alla frequenza dei fotogrammi.

**WriteSample funziona** in modo asincrono e potrebbe non terminare la scrittura dei dati dal buffer prima che l'applicazione sia pronta a chiamare nuovamente il metodo. È quindi importante chiamare **AllocateSample** una volta per ogni chiamata a **WriteSample.** Tuttavia, è possibile rilasciare **l'interfaccia INSSBuffer** immediatamente dopo aver chiamato **WriteSample.**

Dopo aver completato il passaggio degli esempi, chiamare [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).

**Nota** È importante che gli esempi di tutti i flussi nel file siano passati al writer in sincronizzazione tra loro. Ciò significa che, quando possibile, è necessario passare gli esempi al writer in ordine di tempo di presentazione entro la tolleranza di sincronizzazione specificata in [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance). I risultati migliori vengono ottenuti quando i dati vengono recapitati a ogni flusso in unità di un secondo o meno.

Flussi terminerà anche approssimativamente nello stesso momento. Ad esempio, non è consigliabile scrivere un file con un flusso audio di 45 secondi e un flusso video di 50 secondi. Se si codifica un file di questo tipo con input non modificati, alcuni dati audio alla fine del flusso verranno eliminati (anche se si tratta del flusso più breve). Per fare in modo che la codifica dei file funzioni, è necessario aggiungere 5 secondi di silenzio all'input audio in modo che un flusso non venga terminare alcuni secondi prima di un altro. Non è necessario che i tipi di flusso con esempi intermittenti, ad esempio flussi di testo o immagini, siano riempiti in questo modo. Anche i flussi di comandi script devono seguire tutte queste regole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




