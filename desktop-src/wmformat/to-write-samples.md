---
title: Per scrivere esempi
description: Per scrivere esempi
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- ASF (Advanced Systems Format), scrittura di esempi
- ASF (Advanced Systems Format), scrittura di esempi
- ASF (Advanced Systems Format), passaggio di campioni al writer
- ASF (Advanced Systems Format), passaggio di campioni al writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398566"
---
# <a name="to-write-samples"></a>Per scrivere esempi

Dopo aver identificato e configurato gli input per il file che si sta scrivendo, è possibile iniziare a passare gli esempi al writer. Per rendere più efficiente il processo di scrittura, è necessario passare gli esempi in ordine temporale di presentazione, se possibile.

Prima di passare gli esempi, è necessario impostare il writer affinché li accetti chiamando [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Per passare un esempio al writer, seguire questa procedura:

1.  Allocare un buffer e recuperare un puntatore all'interfaccia [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) chiamando [**IWMWriter:: AllocateSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Recuperare l'indirizzo del buffer creato nel passaggio 1 chiamando [**INSSBuffer:: GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer).
3.  Copiare i dati di esempio nella posizione del buffer, assicurandosi che l'esempio passato venga inserito nel buffer allocato. Per copiare i dati, è possibile usare qualsiasi funzione di copia della memoria. Una scelta comune è memcpy, inclusa nella libreria di runtime del linguaggio C standard.
4.  Aggiornare la quantità di dati utilizzati nel buffer in modo da riflettere le dimensioni effettive dell'esempio chiamando [**INSSBuffer:: selength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength).
5.  Passare l'interfaccia del buffer al writer insieme al numero di input e al tempo di campionamento usando il metodo [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) . Tutti gli esempi audio di un input rappresentano la stessa durata del contenuto, pertanto è possibile calcolare l'ora di esempio aggiungendo la durata del campione a un totale parziale. Per i video, è necessario calcolare il tempo in base alla frequenza dei fotogrammi.

**WriteSample** funziona in modo asincrono e potrebbe non terminare la scrittura dei dati dal buffer prima che l'applicazione sia pronta per chiamare nuovamente il metodo. È quindi importante chiamare **AllocateSample** una volta per ogni chiamata a **WriteSample**. Tuttavia, è possibile rilasciare l'interfaccia **INSSBuffer** immediatamente dopo aver chiamato **WriteSample**.

Al termine del passaggio degli esempi, chiamare [**IWMWriter:: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).

**Nota** È importante che gli esempi di tutti i flussi nel file vengano passati al writer in sincronizzazione tra loro. Ovvero, quando possibile, è necessario passare campioni al writer in ordine di tempo di presentazione entro la tolleranza di sincronizzazione specificata in [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance). I risultati migliori si ottengono quando i dati vengono recapitati a ogni flusso in unità di un secondo o meno.

I flussi devono terminare anche approssimativamente allo stesso tempo. Ad esempio, non è consigliabile scrivere un file con un flusso audio di 45 secondi e un flusso video di lunghezza pari a 50 secondi. Se si codifica un file di questo tipo con input non modificati, alcuni dati audio alla fine del flusso verranno eliminati (anche se si tratta del flusso più breve). Per fare in modo che la codifica dei file funzioni, è necessario aggiungere 5 secondi di silenzio all'input audio, in modo che un flusso non termini alcuni secondi prima di un altro. Non è necessario che i tipi di flusso con esempi intermittenti, ad esempio flussi di testo o immagini, vengano riempiti in questo modo. I flussi del comando per script devono seguire anche tutte queste regole.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Interfaccia IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




