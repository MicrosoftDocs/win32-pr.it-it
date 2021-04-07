---
description: Uso del modello di classe DMO
ms.assetid: 5193ad08-aaee-47e3-93eb-a126a66d8f23
title: Uso del modello di classe DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db80017372f11f6c928e0e6a83b591967a84ee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057833"
---
# <a name="using-the-dmo-class-template"></a>Uso del modello di classe DMO

DirectShow include un modello di classe, [**IMediaObjectImpl**](imediaobjectimpl-class-template.md), per l'implementazione di DMOS. Il modello gestisce molte delle attività di "contabilità", ad esempio la convalida dei parametri di input. Utilizzando il modello, è possibile concentrarsi sulle funzionalità specifiche di DMO. Il modello contribuisce inoltre a garantire la creazione di un'implementazione affidabile. Il modello è definito nel file di intestazione Dmoimpl. h, che si trova nella directory di inclusione dell'SDK.

Il modello **IMediaObjectImpl** eredita l'interfaccia [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) . Per creare un DMO usando il modello, definire una nuova classe che deriva da **IMediaObjectImpl**. Il modello implementa tutti i metodi **IMediaObject** . Nella maggior parte dei casi, il modello chiama un metodo privato corrispondente nella classe derivata. Il modello offre le funzionalità seguenti:

-   Verifica dei parametri di base. I metodi del modello verificano che i parametri obbligatori non siano **null**, che gli indici di flusso siano compresi nell'intervallo e che i flag siano validi.
-   Blocco. I metodi del modello chiamano due metodi interni, **Lock** e **Unlock**, per serializzare le operazioni su DMO. Questa funzionalità garantisce che DMO sia thread-safe.
-   Tipi di supporto. Il modello archivia i tipi di supporto impostati dal client e fornisce i metodi delle funzioni di accesso per i tipi di supporto.
-   Streaming. Il modello impedisce lo streaming finché il client non ha impostato i tipi di supporto per tutti i flussi non facoltativi. Garantisce inoltre che il metodo [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources) venga chiamato prima dell'inizio del flusso, garantendo così l'allocazione delle risorse.

La classe derivata deve implementare l'interfaccia **IUnknown** ; il modello non fornisce questa interfaccia. È possibile utilizzare il Active Template Library (ATL) per implementare **IUnknown** oppure è possibile fornire altre implementazioni. Il modello non implementa inoltre il meccanismo di blocco. La classe derivata deve implementare i metodi **Lock** e **Unlock** . Se si crea la classe utilizzando ATL, è possibile utilizzare le implementazioni ATL predefinite.

**Dichiarazione della classe derivata**

Il modello di classe **IMediaObjectImpl** viene dichiarato nel modo seguente:


```C++
template <class _DERIVED_, int NUMBEROFINPUTS, int NUMBEROFOUTPUTS>
class IMediaObjectImpl : public ImediaObject
```



I tre parametri di modello sono \_ Derived \_ , NUMBEROFINPUTS e NUMBEROFOUTPUTS. Impostare \_ derivato \_ uguale al nome della classe. Gli altri due parametri definiscono il numero di flussi di input e di output nell'DMO. Ad esempio, per creare una classe DMO denominata CMyDmo che supporta un flusso di input e due flussi di output, usare la dichiarazione seguente:


```C++
class CMyDmo : public IMediaObjectImpl<CMyDmo, 1, 2>
```



Nella parte restante di questa sezione viene descritto il modo in cui il modello implementa i vari metodi in **IMediaObject**.

**Metodi per l'impostazione di tipi di supporto**

I metodi seguenti impostano o recuperano i tipi di supporto in DMO:

-   **GetInputType**, **GetOutputType**. Questi metodi restituiscono i tipi di supporto preferiti, per numero di flusso e indice di tipo. Il modello chiama **InternalGetInputType** o **InternalGetOutputType** sulla classe derivata.
-   **SetInputType**, **SetOutputType**. Questi metodi impostano il tipo di supporto in un flusso, testano un tipo di supporto o cancellano un tipo di supporto. Per convalidare il tipo di supporto, il modello chiama **InternalCheckInputType** o **InternalCheckOutputType** nella classe derivata. La classe derivata restituisce S \_ OK per accettare il tipo o DMO \_ E \_ INVALIDTYPE per rifiutare il tipo. Il modello gestisce l'impostazione o la cancellazione del tipo di supporto.
-   **GetInputCurrentType**, **GetOutputCurrentType**. Questi metodi restituiscono il tipo di supporto corrente per un flusso o \_ il \_ tipo DMO E \_ non \_ è impostato se non è impostato alcun tipo. Il modello implementa completamente questi metodi.

**Metodi informativi**

I metodi seguenti forniscono informazioni su DMO.

-   **GetInputMaxLatency**, **SetInputMaxLatency**. Questi metodi recuperano o impostano la latenza massima. Il modello chiama **InternalGetInputMaxLatency** o **InternalSetInputMaxLatency** sulla classe derivata.
-   **GetInputSizeInfo**, **GetOutputSizeInfo**. Questi metodi restituiscono i requisiti del buffer DMO per un flusso specificato. Se non è stato impostato alcun tipo di supporto per quel flusso, il modello restituisce DMO \_ E \_ Type \_ non \_ impostato. In caso contrario, chiama **InternalGetInputSizeInfo** o **InternalGetOutputSizeInfo** sulla classe derivata.
-   **GetInputStreamInfo**, **GetOutputStreamInfo**. Questi metodi restituiscono diversi flag che indicano il modo in cui il client deve formattare i dati. Il modello chiama **InternalGetInputStreamInfo** o **InternalGetOutputStreamInfo** sulla classe derivata.
-   **GetStreamCount**. Questo metodo restituisce il numero di flussi di input e di output. Il modello implementa questo metodo, usando i parametri del modello.

**Metodi per l'allocazione delle risorse**

-   Il metodo **AllocateStreamingResources** alloca le risorse necessarie a DMO prima che inizi il flusso. Il metodo **FreeStreamingResources** rilascia le stesse risorse. Il modello chiama rispettivamente **InternalAllocateStreamingResources** e **InternalFreeStreamingResources**.

Non è necessario che il client di DMO chiami questi metodi, ma il modello chiama automaticamente **AllocateStreamingResources** prima dell'avvio del flusso. Pertanto, DMO può presumere che le risorse siano state allocate correttamente nel momento in cui viene chiamato **ProcessInput** . Il DMO deve chiamare **FreeStreamingResources** nel relativo distruttore.

Inoltre, quando il modello chiama **InternalAllocateStreamingResources**, imposta un flag interno, in modo che non chiami di nuovo il metodo fino a quando non viene chiamato **InternalFreeStreamingResources**. Ciò garantisce che le risorse non vengano riallocate accidentalmente, causando perdite di memoria.

**Metodi per lo streaming**

Per eseguire lo streaming dei dati, vengono usati i metodi seguenti:

-   **GetInputStatus**. Questo metodo indica se l'oggetto DMO è in grado di accettare l'input in questo momento. Il modello chiama **InternalAcceptingInput** sulla classe derivata. Se DMO è in grado di accettare l'input, la classe derivata restituisce \_ OK e il modello imposta \_ il \_ bit di input DMO STATUSF i \_ \_ dati nel parametro *dwFlags* . In caso contrario, la classe derivata restituisce \_ false e il modello imposta *dwFlags* su zero.
-   **ProcessInput**. Questo metodo elabora un buffer di input. Il modello chiama **AllocateStreamingResources**, descritto in precedenza. Chiama quindi **InternalAcceptingInput** sulla classe derivata. Se DMO può accettare nuovo input, il modello chiama **InternalProcessInput**.
-   **ProcessOutput**. Questo metodo elabora un set di buffer di output, un buffer per ogni flusso di output. Il modello chiama **AllocateStreamingResources** e quindi **InternalProcessOutput**.
-   **Discontinuità**. Questo metodo segnala una discontinuità in un flusso di input. Il modello chiama **InternalAcceptingInput** sulla classe derivata. Se il metodo restituisce S \_ OK, il modello chiama **InternalDiscontinuity** sulla classe derivata.
-   **Scarica**. Questo metodo Scarica DMO. Il modello chiama **InternalFlush** sulla classe derivata. Il DMO deve rimuovere tutti i buffer di input che ancora conserva per essere elaborati.

Il modello non fornisce alcun supporto diretto per l'interfaccia [**IMediaObjectInPlace**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobjectinplace) .

**Metodi per il blocco**

Il blocco viene usato per proteggere lo stato di DMO in un ambiente a thread multipli. In un progetto ATL il metodo [**IMediaObject:: Lock**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-lock) causa un conflitto di nome con il metodo di **blocco** ATL. Per risolvere il conflitto, il modello Rinomina il metodo **IMediaObject** in **DMOLock**. Quando si compila la classe derivata, definire Correggi \_ il \_ nome del blocco prima di includere il file di intestazione DMO. h:


```C++
#define FIX_LOCK_NAME
#include <dmo.h>
```



Questa direttiva fa in modo che il preprocessore sostituisca **DMOLock** per il **blocco** nella dichiarazione dell'interfaccia **IMediaObject** . Le applicazioni possono comunque richiamare il metodo utilizzando il **blocco** del nome, perché l'ordine vtable non cambia. Il metodo **DMOLock** chiama **Lock** o **Unlock** sulla classe derivata. Se si utilizza ATL per implementare la classe derivata, questi metodi sono già definiti da ATL, pertanto non è necessario alcun codice aggiuntivo. Se non si utilizza ATL, è necessario fornire i metodi **Lock** e **Unlock** nella classe derivata.

Il modello blocca automaticamente il DMO in ognuno dei metodi **IMediaObject** . Potrebbe essere necessario che la classe derivata blocchi DMO all'interno di altri metodi pubblici implementati, ad esempio se supporta **IMediaObjectInPlace**. Il modello di classe fornisce anche una classe helper interna, [**IMediaObjectImpl:: Lockit**](imediaobjectimpl-lockit.md), che è utile per bloccare e sbloccare DMO.

**Summary**

Per i metodi **IMediaObject** seguenti, il modello chiama un metodo corrispondente con la stessa firma nella classe derivata. La classe derivata deve implementare ognuno dei metodi illustrati nella seconda colonna.



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



 

Per i metodi **IMediaObject** rimanenti, non esiste una corrispondenza uno-a-uno tra i metodi dei modelli e i metodi della classe derivata. Nella tabella seguente vengono riepilogati i metodi completamente implementati dal modello e quali metodi chiamano altri metodi sulla classe derivata.



| Metodo IMediaObject                   | Metodo della classe derivata                                                             |
|---------------------------------------|----------------------------------------------------------------------------------|
| **GetInputCurrentType**               | Completamente implementato                                                                |
| **GetOutputCurrentType**              | Completamente implementato                                                                |
| **GetStreamCount**                    | Completamente implementato                                                                |
| **GetInputStatus**                    | [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))        |
| **Lock** (implementato come **DMOLock**) | [**Blocco**](/previous-versions/ms809100(v=msdn.10)), [ **sblocco**](/previous-versions/ms809101(v=msdn.10)) |
| **SetInputType**                      | [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))        |
| **SetOutputType**                     | [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10))      |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Modello di classe IMediaObjectImpl**](imediaobjectimpl-class-template.md)
</dt> <dt>

[Scrittura di un DMO](writing-a-dmo.md)
</dt> </dl>

 

 
