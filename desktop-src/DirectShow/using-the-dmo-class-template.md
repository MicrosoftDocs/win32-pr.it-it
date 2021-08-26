---
description: Uso del modello DMO classe
ms.assetid: 5193ad08-aaee-47e3-93eb-a126a66d8f23
title: Uso del modello DMO classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 205ee51953aff35ef5b05790b45fcd0bdf3bcd753239a521e40ca796c21b0a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130901"
---
# <a name="using-the-dmo-class-template"></a>Uso del modello DMO classe

DirectShow include un modello di classe, [**IMediaObjectImpl,**](imediaobjectimpl-class-template.md)per l'implementazione di DMO. Il modello gestisce molte delle attività di "contabilità", ad esempio la convalida dei parametri di input. Usando il modello, è possibile concentrarsi sulle funzionalità specifiche per l'DMO. Inoltre, il modello consente di creare un'implementazione affidabile. Il modello è definito nel file di intestazione Dmoimpl.h, che si trova nella directory Include dell'SDK.

Il **modello IMediaObjectImpl** eredita l'interfaccia [**IMediaObject.**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) Per creare un DMO usando il modello, definire una nuova classe che deriva da **IMediaObjectImpl**. Il modello implementa tutti i **metodi IMediaObject.** Nella maggior parte dei casi, il modello chiama un metodo privato corrispondente nella classe derivata. Il modello offre le funzionalità seguenti:

-   Controllo dei parametri di base. I metodi del modello verificano che i parametri obbligatori non siano **NULL,** che gli indici di flusso siano entro l'intervallo e che i flag siano validi.
-   Blocco. I metodi del modello chiamano due metodi interni, **Lock** e **Unlock,** per serializzare le operazioni sul DMO. Questa funzionalità garantisce che il DMO sia thread-safe.
-   Tipi di supporti. Il modello archivia i tipi di supporti impostati dal client e fornisce metodi della funzione di accesso per i tipi di supporti.
-   Streaming. Il modello impedisce lo streaming fino a quando il client non ha impostato i tipi di supporti per tutti i flussi non facoltativi. Garantisce inoltre che il metodo [**IMediaObject::AllocateStreamingResources**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) venga chiamato prima dell'inizio del flusso, garantendo così l'allocazione delle risorse.

La classe derivata deve implementare **l'interfaccia IUnknown.** il modello non fornisce questa interfaccia. È possibile usare il Active Template Library (ATL) per implementare **IUnknown** oppure è possibile fornire un'altra implementazione. Il modello inoltre non implementa il meccanismo di blocco. La classe derivata deve implementare i **metodi Lock** **e Unlock.** Se si crea la classe usando ATL, è possibile usare le implementazioni ATL predefinite.

**Dichiarazione della classe derivata**

Il **modello di classe IMediaObjectImpl** viene dichiarato come segue:


```C++
template <class _DERIVED_, int NUMBEROFINPUTS, int NUMBEROFOUTPUTS>
class IMediaObjectImpl : public ImediaObject
```



I tre parametri di modello \_ sono \_ DERIVED, NUMBEROFINPUTS e NUMBEROFOUTPUTS. Impostare \_ DERIVED uguale al nome della \_ classe. Gli altri due parametri definiscono il numero di flussi di input e di flussi di output nel DMO. Ad esempio, per creare una DMO denominata CMyDmo che supporta un flusso di input e due flussi di output, usare la dichiarazione seguente:


```C++
class CMyDmo : public IMediaObjectImpl<CMyDmo, 1, 2>
```



Nella parte restante di questa sezione viene descritto come il modello implementa i vari metodi in **IMediaObject**.

**Metodi per l'impostazione dei tipi di supporti**

I metodi seguenti impostano o recuperano tipi di supporti nel DMO:

-   **GetInputType**, **GetOutputType**. Questi metodi restituiscono i tipi di supporti preferiti, in base al numero di flusso e all'indice del tipo. Il modello chiama **InternalGetInputType** **o InternalGetOutputType** nella classe derivata.
-   **SetInputType**, **SetOutputType**. Questi metodi impostano il tipo di supporto in un flusso, testano un tipo di supporto o cancellano un tipo di supporto. Per convalidare il tipo di supporto, il modello chiama **InternalCheckInputType** **o InternalCheckOutputType** nella classe derivata. La classe derivata restituisce S OK per accettare il tipo o DMO \_ \_ E \_ INVALIDTYPE per rifiutare il tipo. Il modello gestisce l'impostazione o la cancellazione del tipo di supporto.
-   **GetInputCurrentType**, **GetOutputCurrentType**. Questi metodi restituiscono il tipo di supporto corrente per un flusso o DMO E TYPE NOT SET se non è impostato \_ \_ alcun \_ \_ tipo. Il modello implementa completamente questi metodi.

**Metodi in informazioni**

I metodi seguenti forniscono informazioni sull'DMO.

-   **GetInputMaxLatency**, **SetInputMaxLatency**. Questi metodi recuperano o impostano la latenza massima. Il modello chiama **InternalGetInputMaxLatency** **o InternalSetInputMaxLatency** nella classe derivata.
-   **GetInputSizeInfo**, **GetOutputSizeInfo**. Questi metodi restituiscono i DMO del buffer per un flusso specificato. Se nel flusso non è stato impostato alcun tipo di supporto, il modello restituisce DMO \_ E \_ TYPE NOT \_ \_ SET. In caso contrario, chiama **InternalGetInputSizeInfo** **o InternalGetOutputSizeInfo** nella classe derivata.
-   **GetInputStreamInfo**, **GetOutputStreamInfo**. Questi metodi restituiscono vari flag che indicano come il client deve formattare i dati. Il modello chiama **InternalGetInputStreamInfo** **o InternalGetOutputStreamInfo** nella classe derivata.
-   **GetStreamCount**. Questo metodo restituisce il numero di flussi di input e output. Il modello implementa questo metodo, usando i parametri del modello.

**Metodi per l'allocazione delle risorse**

-   Il **metodo AllocateStreamingResources** alloca tutte le risorse necessarie DMO prima dell'inizio del flusso. Il **metodo FreeStreamingResources** rilascia le stesse risorse. Il modello chiama **rispettivamente InternalAllocateStreamingResources** **e InternalFreeStreamingResources.**

Il client dell'DMO non è necessario per chiamare questi metodi, ma il modello chiama automaticamente **AllocateStreamingResources** prima dell'avvio del flusso. Pertanto, il DMO può presupporre che le risorse siano state allocate correttamente al momento della chiamata **a ProcessInput.** Il DMO deve chiamare **FreeStreamingResources** nel relativo distruttore.

Inoltre, quando il modello chiama **InternalAllocateStreamingResources,** imposta un flag interno, in modo che non chiami di nuovo il metodo fino a quando non viene chiamato **InternalFreeStreamingResources**. In questo modo si garantisce che le risorse non vengano riallocte accidentalmente e ciò potrebbe causare perdite di memoria.

**Metodi per lo streaming**

Per trasmettere i dati vengono usati i metodi seguenti:

-   **GetInputStatus**. Questo metodo indica se l'DMO può accettare l'input in questo momento. Il modello chiama **InternalAcceptingInput** sulla classe derivata. Se il DMO può accettare l'input, la classe derivata restituisce S OK e il modello imposta il bit DMO INPUT STATUSF ACCEPT DATA nel \_ \_ parametro \_ \_ \_ *dwFlags.* In caso contrario, la classe derivata restituisce S \_ FALSE e il modello imposta *dwFlags* su zero.
-   **ProcessInput**. Questo metodo elabora un buffer di input. Il modello chiama **AllocateStreamingResources**, descritto in precedenza. Chiama quindi **InternalAcceptingInput** sulla classe derivata. Se il DMO può accettare un nuovo input, il modello chiama **InternalProcessInput**.
-   **ProcessOutput**. Questo metodo elabora un set di buffer di output, un buffer per ogni flusso di output. Il modello chiama **AllocateStreamingResources** e quindi **InternalProcessOutput**.
-   **Discontinuità**. Questo metodo segnala una discontinuità in un flusso di input. Il modello chiama **InternalAcceptingInput** sulla classe derivata. Se il metodo restituisce S \_ OK, il modello chiama **InternalDiscontinuity** nella classe derivata.
-   **Scaricare**. Questo metodo scarica il DMO. Il modello chiama **InternalFlush** sulla classe derivata. Il DMO deve eliminare tutti i buffer di input che contiene ancora per l'elaborazione.

Il modello non fornisce alcun supporto diretto per [**l'interfaccia IMediaObjectInPlace.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace)

**Metodi per il blocco**

Il blocco viene usato per proteggere lo stato DMO in un ambiente multithreading. In un progetto ATL, il [**metodo IMediaObject::Lock**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-lock) causa un conflitto di nomi con il metodo BLOCCO **ATL.** Per risolvere il conflitto, il modello rinomina il **metodo IMediaObject** in **DMOLock**. Quando si compila la classe derivata, definire FIX \_ LOCK NAME prima di includere il file di intestazione \_ Dmo.h:


```C++
#define FIX_LOCK_NAME
#include <dmo.h>
```



Questa direttiva fa sì che il preprocessore **sostituisca DMOLock** **con Lock** nella dichiarazione **dell'interfaccia IMediaObject.** Le applicazioni possono comunque richiamare il metodo usando il nome **Lock**, perché l'ordine vtable non cambia. Il **metodo DMOLock** chiama **Lock** o **Unlock** sulla classe derivata. Se si usa ATL per implementare la classe derivata, questi metodi sono già definiti da ATL, quindi non è necessario codice aggiuntivo. Se non si usa ATL, è necessario fornire **i metodi Lock** e **Unlock** nella classe derivata.

Il modello blocca automaticamente il DMO in ognuno dei **metodi IMediaObject.** La classe derivata potrebbe dover bloccare il DMO all'interno di altri metodi pubblici implementati da tale classe( ad esempio, se supporta **IMediaObjectInPlace**). Il modello di classe fornisce anche una classe helper interna, [**IMediaObjectImpl::LockIt,**](imediaobjectimpl-lockit.md)utile per bloccare e sbloccare il DMO.

**Summary**

Per i metodi **IMediaObject** seguenti, il modello chiama un metodo corrispondente con la stessa firma nella classe derivata. La classe derivata deve implementare ognuno dei metodi indicati nella seconda colonna.



| Metodo IMediaObject            | Metodo della classe derivata                   |
|--------------------------------|----------------------------------------|
| **AllocateStreamingResources** | **InternalAllocateStreamingResources** |
| **Discontinuità**              | **InternalDiscontinuity**              |
| **Svuotamento**                      | **InternalFlush**                      |
| **FreeStreamingResources**     | **InternalFreeStreamingResources**     |
| **GetInputMaxLatency**         | **InternalGetInputMaxLatency**         |
| **GetInputSizeInfo**           | **InternalGetInputSizeInfo**           |
| **GetInputStreamInfo**         | **InternalGetInputStreamInfo**         |
| **GetInputType**               | **InternalGetInputType**               |
| **GetOutputSizeInfo**          | **InternalGetOutputSizeInfo**          |
| **GetOutputStreamInfo**        | **InternalGetOutputStreamInfo**        |
| **GetOutputType**              | **InternalGetOutputType**              |
| **ProcessInput**               | **InternalProcessInput**               |
| **ProcessOutput**              | **InternalProcessOutput**              |
| **SetInputMaxLatency**         | **InternalSetInputMaxLatency**         |



 

Per i metodi **IMediaObject rimanenti,** non esiste una corrispondenza uno-a-uno tra i metodi modello e i metodi della classe derivata. Nella tabella seguente vengono riepilogati i metodi completamente implementati dal modello e i metodi che chiamano altri metodi nella classe derivata.



| Metodo IMediaObject                   | Metodo della classe derivata                                                             |
|---------------------------------------|----------------------------------------------------------------------------------|
| **GetInputCurrentType**               | Completamente implementato                                                                |
| **GetOutputCurrentType**              | Completamente implementato                                                                |
| **GetStreamCount**                    | Completamente implementato                                                                |
| **GetInputStatus**                    | [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))        |
| **Lock** (implementato come **DMOLock**) | [**Blocca,**](/previous-versions/ms809100(v=msdn.10)) [ **Sblocca**](/previous-versions/ms809101(v=msdn.10)) |
| **SetInputType**                      | [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))        |
| **SetOutputType**                     | [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modello di classe IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> <dt>

[Scrittura di un DMO](writing-a-dmo.md)
</dt> </dl>

 

 
