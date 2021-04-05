---
description: Elaborazione di dati in un DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Elaborazione di dati in un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9f5d5d820dc1467c25f9d411d46a9c66935e8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876653"
---
# <a name="processing-data-in-a-dmo"></a>Elaborazione di dati in un DMO

In questa sezione viene illustrato come elaborare un flusso di dati utilizzando DMO. I passaggi elencati in questa sezione rappresentano il comportamento predefinito. tutti DMOs devono supportare i metodi descritti qui. Questi metodi usano buffer distinti per l'input e l'output. Alcuni DMOs supportano anche l'elaborazione sul posto, usando un singolo buffer. Per ulteriori informazioni sull'elaborazione sul posto, vedere [elaborazione sul posto](in-place-processing.md).

**Allocazione di buffer**

Il client è responsabile di tutte le allocazioni di buffer. Dopo aver impostato i tipi di supporto su DMO, eseguire una query su DMO per i requisiti del buffer di ogni flusso. Questi possono variare a seconda del tipo di supporto. Per ogni flusso, chiamare il metodo [**IMediaObject:: GetInputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) o [**IMediaObject:: GetOutputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) . Questi metodi restituiscono le informazioni seguenti:

-   Dimensioni minime del buffer, in byte.
-   Eventuali requisiti di allineamento. Un buffer è allineato se l'indirizzo iniziale è un multiplo di un numero intero specificato.
-   Quantità massima di dati che DMO terrà per lookahead. Questo numero si applica solo ai flussi di input. Per alcuni tipi di dati (ad esempio, la codifica MPEG), è possibile che un DMO debba essere in attesa nel flusso. Il valore lookahead indica la quantità di dati di input richiesta da DMO prima che possa produrre l'output.

Il client deve allocare buffer che soddisfano questi requisiti. Inoltre, DMO potrebbe avere requisiti relativi al modo in cui il client include i dati di input. Ad esempio, DMO potrebbe richiedere a ogni buffer di contenere esattamente un campione (o un fotogramma video). Per determinare questi requisiti, chiamare il metodo [**IMediaObject:: GetInputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) . Il metodo [**IMediaObject:: GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) restituisce informazioni simili su un flusso di output.

Nel modello di streaming predefinito, il client non passa i puntatori del buffer non elaborato a DMO. USA invece un oggetto COM leggero che espone l'interfaccia [**IMediaBuffer**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) . L'interfaccia **IMediaBuffer** funge da wrapper com per un blocco di memoria. Poiché si tratta di un oggetto COM, supporta il conteggio dei riferimenti, che consente di garantire che i buffer non vengano rilasciati mentre sono ancora in uso.

> [!Note]  
> L'interfaccia **IMediaBuffer** offre una funzione simile all'interfaccia **IMediaSample** in DirectShow.

 

Il client deve implementare l'oggetto **IMediaBuffer** . Per ulteriori informazioni, vedere [implementazione di IMediaBuffer](implementing-imediabuffer.md).

**Elaborazione dei dati**

Per elaborare i dati, eseguire le operazioni seguenti:

1.  Per ogni flusso di input, riempire un buffer con i dati di input.
2.  Chiamare [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) per il recapito di ogni buffer.
3.  Chiamare [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) per elaborare i dati. Questo metodo accetta una matrice di buffer, uno per ogni flusso di output.
4.  Ripetere fino a quando non sono presenti altri dati di input.

Il metodo **ProcessInput** accetta input per un flusso alla volta. In genere il metodo viene restituito immediatamente e DMO include un conteggio dei riferimenti nell'oggetto **IMediaBuffer** . Rilascia l'oggetto dopo l'elaborazione di tutti i dati nel buffer o quando l'applicazione Scarica DMO. Non riutilizzare un buffer finché non viene rilasciato da DMO. Per determinare se un flusso di input può accettare più dati, chiamare il metodo [**IMediaObject:: GetInputStatus**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) . Questo metodo restituisce il \_ flag di input DMO \_ STATUSF \_ Accept \_ data se il flusso può accettare più input.

Il metodo **ProcessOutput** genera l'output per tutti i flussi di output in una sola volta. L'applicazione passa una matrice di strutture [**del \_ \_ \_ buffer dei dati di output DMO**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) , una per ogni flusso di output. Ogni struttura della matrice ha un puntatore a un oggetto **IMediaBuffer** . DMO scrive il maggior quantità di dati di output possibile nei buffer. Vengono inoltre impostati diversi flag per segnalare lo stato dell'operazione. Il \_ \_ flag di output DMO \_ BUFFERF data \_ incomplete indica che DMO può produrre più output dall'input esistente. In tal caso, il client può chiamare nuovamente **ProcessOutput** . In caso contrario, deve chiamare **ProcessInput** con più dati di input. DMO non modifica mai i dati nei buffer di input. scrive solo nei buffer di output.

Dopo aver recapitato tutti i dati in un flusso di input, chiamare il metodo [**IMediaObject::D di continuità**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) . DMO non accetta ulteriori input per tale flusso fino a quando non si elabora l'output rimanente (o si Scarica DMO).

In qualsiasi momento dopo l'avvio del flusso, DMO è in grado di ricevere input o produrre output o entrambi. Di conseguenza, **GetInputStatus** restituisce DMO \_ input \_ STATUSF \_ accetta \_ dati oppure **ProcessOutput** restituisce DMO \_ output \_ data \_ BUFFERF \_ incompleto. L'applicazione mantiene il flusso di dati testando questi flag e chiamando di conseguenza **ProcessInput** o **ProcessOutput** . Per interrompere il flusso di dati, chiamare il metodo [**IMediaObject:: Flush**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) . Questo metodo fa in modo che DMO elimini tutti i buffer che contiene internamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hosting diretto di un DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[Elaborazione sul posto](in-place-processing.md)
</dt> </dl>

 

 



