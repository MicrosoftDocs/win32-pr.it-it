---
description: Elaborazione di dati in un DMO
ms.assetid: 715482d9-23f4-40d0-9c09-7a81e148c543
title: Elaborazione di dati in un DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd4dd05df960bd27b34eb55b604c8469e7bbaedd57ea928f5b4f412ad4bff04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748241"
---
# <a name="processing-data-in-a-dmo"></a>Elaborazione di dati in un DMO

Questa sezione illustra come elaborare un flusso di dati usando un DMO. I passaggi elencati in questa sezione sono il comportamento predefinito. Tutti gli oggetti DMO devono supportare i metodi descritti qui. Questi metodi usano buffer separati per l'input e l'output. Alcuni DMO supportano anche l'elaborazione sul posto, usando un singolo buffer. Per altre informazioni sull'elaborazione sul posto, vedere [Elaborazione sul posto.](in-place-processing.md)

**Allocazione di buffer**

Il client è responsabile di tutte le allocazioni di buffer. Dopo aver impostato i tipi di supporti nel DMO, eseguire una query DMO per i requisiti di buffer di ogni flusso. Questi valori possono variare a seconda del tipo di supporto. Per ogni flusso, chiamare [**il metodo IMediaObject::GetInputSizeInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputsizeinfo) o [**IMediaObject::GetOutputSizeInfo.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputsizeinfo) Questi metodi restituiscono le informazioni seguenti:

-   Dimensioni minime del buffer, in byte.
-   Requisiti di allineamento, se presenti. Un buffer è allineato se l'indirizzo iniziale è un multiplo di un numero intero specificato.
-   Quantità massima di dati che il DMO contenerà per lookahead. Questo numero si applica solo ai flussi di input. Per alcuni tipi di dati , ad esempio la codifica MPEG, potrebbe essere necessario DMO un flusso. Il valore lookahead indica la quantità di dati di input DMO necessaria per poter produrre l'output.

Il client deve allocare buffer che soddisfano questi requisiti. Inoltre, il DMO potrebbe avere requisiti relativi alla modalità di creazione del pacchetto dei dati di input da parte del client. Ad esempio, il DMO potrebbe richiedere che ogni buffer contenga esattamente un campione (o fotogramma video). Per determinare questi requisiti, chiamare [**il metodo IMediaObject::GetInputStreamInfo.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstreaminfo) Il [**metodo IMediaObject::GetOutputStreamInfo**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputstreaminfo) restituisce informazioni simili su un flusso di output.

Nel modello di flusso predefinito, il client non passa puntatori del buffer non elaborati al DMO. Usa invece un oggetto COM leggero che espone [**l'interfaccia IMediaBuffer.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediabuffer) **L'interfaccia IMediaBuffer** funge da wrapper COM per un blocco di memoria. Poiché si tratta di un oggetto COM, supporta il conteggio dei riferimenti, che consente di garantire che i buffer non vengono rilasciati mentre sono ancora in uso.

> [!Note]  
> **L'interfaccia IMediaBuffer** svolge una funzione simile all'interfaccia **IMediaSample** in DirectShow.

 

Il client deve implementare **l'oggetto IMediaBuffer.** Per altre informazioni, vedere [Implementazione di IMediaBuffer.](implementing-imediabuffer.md)

**Elaborazione dei dati**

Per elaborare i dati, eseguire le operazioni seguenti:

1.  Per ogni flusso di input, compilare un buffer con i dati di input.
2.  Chiamare [**IMediaObject::P rocessInput per**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processinput) recapitare ogni buffer.
3.  Chiamare [**IMediaObject::P rocessOutput per**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-processoutput) elaborare i dati. Questo metodo accetta una matrice di buffer, uno per ogni flusso di output.
4.  Ripetere fino a quando non sono presenti altri dati di input.

Il **metodo ProcessInput** accetta l'input per un flusso alla volta. In genere il metodo restituisce immediatamente e il DMO contiene un conteggio dei riferimenti per **l'oggetto IMediaBuffer.** Rilascia l'oggetto dopo l'elaborazione di tutti i dati nel buffer o quando l'applicazione scarica il DMO. Non usare nuovamente un buffer fino a quando il DMO non lo ha rilasciato. Per determinare se un flusso di input può accettare più dati, chiamare il [**metodo IMediaObject::GetInputStatus.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputstatus) Questo metodo restituisce il flag DMO \_ INPUT \_ STATUSF \_ ACCEPT DATA se il flusso può accettare più \_ input.

Il **metodo ProcessOutput** genera l'output per tutti i flussi di output contemporaneamente. L'applicazione passa una matrice di [**DMO \_ OUTPUT DATA \_ \_ BUFFER,**](/previous-versions/windows/desktop/api/Mediaobj/ns-mediaobj-dmo_output_data_buffer) una per ogni flusso di output. Ogni struttura nella matrice ha un puntatore a un **oggetto IMediaBuffer.** Il DMO scrive il maggior numero possibile di dati di output nei buffer. Imposta inoltre diversi flag per segnalare lo stato dell'operazione. Il flag OUTPUT DATA BUFFERF INCOMPLETE DMO indica che il DMO \_ può produrre più output \_ \_ \_ dall'input esistente. In tal caso, il client può chiamare **di nuovo ProcessOutput.** In caso contrario, deve chiamare **ProcessInput con** più dati di input. Il DMO non modifica mai i dati nei buffer di input; scrive solo nei buffer di output.

Dopo aver recapitato tutti i dati a un flusso di input, chiamare il metodo [**IMediaObject::D iscontinuity.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-discontinuity) Il DMO accetta ulteriori input per il flusso fino a quando non si elabora l'output rimanente (o si scarica il DMO).

In qualsiasi momento dopo l'inizio del flusso, il DMO può ricevere input o produrre output o entrambi. Pertanto, **GetInputStatus** restituisce DMO INPUT STATUSF ACCEPT DATA oppure \_ \_ \_ \_ **ProcessOutput** restituisce DMO \_ OUTPUT DATA \_ \_ BUFFERF \_ INCOMPLETE. L'applicazione mantiene il flusso dei dati testando questi flag e chiamando **ProcessInput** **o ProcessOutput di** conseguenza. Per interrompere il flusso di dati, chiamare [**il metodo IMediaObject::Flush.**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-flush) Questo metodo fa in modo DMO eliminare tutti i buffer che contiene internamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Hosting diretto di un DMO](directly-hosting-a-dmo.md)
</dt> <dt>

[Elaborazione sul posto](in-place-processing.md)
</dt> </dl>

 

 



