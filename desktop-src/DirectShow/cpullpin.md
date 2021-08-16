---
description: La classe CPullPin fornisce il supporto per i pin di input che estraeno i dati tramite l'interfaccia IAsyncReader.
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: Classe CPullPin (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d70217fa60afdae3f588f98ecbe61a728ace6ec0b0d78859f55cd241cbc00e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119330847"
---
# <a name="cpullpin-class"></a>Classe CPullPin

![Gerarchia di classi cpullpin](images/pulpin01.png)

La `CPullPin` classe fornisce il supporto per i pin di input che estraeno i dati tramite [**l'interfaccia IAsyncReader.**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) Utilizzare questa classe se si implementa un filtro che usa il modello pull per richiedere dati dal filtro upstream. Per altre informazioni, vedere Data Flow in Filter Graph and Pull Model (Modello di Graph e pull).

Questa classe non deriva da **CBasePin** o implementa l'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) e alcuni nomi di metodo sono in conflitto con **IPin,** quindi è meglio usare come oggetto helper all'interno del pin. Per usare questa classe, eseguire le operazioni seguenti:

1.  Derivare una classe helper da `CPullPin` e derivare una classe pin di input **da CBasePin.** Dichiarare un'istanza `CPullPin` dell'oggetto come variabile membro della classe pin.
2.  Eseguire [**l'override del metodo CBasePin::CheckConnect**](cbasepin-checkconnect.md) per [**chiamare CPullPin::Connessione**](cpullpin-connect.md). Questo metodo esegue una query sull'altro pin **per IAsyncReader.**
3.  Eseguire [**l'override del metodo CBasePin::BreakConnect**](cbasepin-breakconnect.md) per chiamare [**CPullPin::D isconnect.**](cpullpin-disconnect.md)
4.  Eseguire [**l'override del metodo CBasePin::Active**](cbasepin-active.md) per [**chiamare CPullPin::Active.**](cpullpin-active.md) Questo metodo avvia un thread di lavoro che esegue il pull dei campioni dal filtro upstream. Quando i pin si connettono, è possibile specificare se il thread di lavoro deve effettuare richieste di lettura asincrone o sincrone.
5.  Eseguire [**l'override del metodo CBasePin::Inactive**](cbasepin-inactive.md) per [**chiamare CPullPin::Inactive.**](cpullpin-inactive.md) Questo metodo arresta il thread di lavoro.
6.  Implementare il metodo [**CPullPin::Receive**](cpullpin-receive.md) virtuale puro per elaborare gli esempi in ingresso e recapitarli a valle.
7.  Per impostare le posizioni di arresto e avvio o per cercare il flusso, chiamare il [**metodo CPullPin::Seek.**](cpullpin-seek.md) Questo metodo sospende il thread di lavoro e scarica il grafico dei filtri.
8.  Implementare i metodi [**virtuali puri CPullPin::EndOfStream**](cpullpin-endofstream.md), [**CPullPin::BeginFlush**](cpullpin-beginflush.md)e [**CPullPin::EndFlush,**](cpullpin-endflush.md) come descritto nelle osservazioni per tali metodi.
9.  Implementare il metodo [**CPullPin::OnError**](cpullpin-onerror.md) virtuale puro per gestire gli errori di streaming.



| Variabili membro pubbliche                             | Descrizione                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**m \_ pAlloc**](cpullpin-m-palloc.md)              | Puntatore **all'interfaccia IMemAllocator** dell'allocatore di memoria.                   |
| Metodi pubblici                                      | Descrizione                                                                           |
| [**Attivo**](cpullpin-active.md)                   | Crea un thread di lavoro che esegue il pull dei dati dal pin di output.                          |
| [**AlignDown**](cpullpin-aligndown.md)             | Tronca un valore a un limite di allineamento specificato.                                  |
| [**AlignUp**](cpullpin-alignup.md)                 | Arrotonda un valore per e per e per e per un limite di allineamento specificato.                                  |
| [**Connettere**](cpullpin-connect.md)                 | Completa una connessione al pin di output.                                             |
| [**CPullPin**](cpullpin-cpullpin.md)               | Metodo del costruttore.                                                                   |
| [**~CPullPin**](cpullpin--cpullpin.md)             | Metodo del distruttore. Virtuale.                                                           |
| [**DecideAllocator**](cpullpin-decideallocator.md) | Negozia un allocatore con il pin di output. Virtuale.                                 |
| [**Disconnetti**](cpullpin-disconnect.md)           | Beaks la connessione con il pin di output.                                             |
| [**Durata**](cpullpin-duration.md)               | Recupera la durata del flusso.                                                 |
| [**GetReader**](cpullpin-getreader.md)             | Restituisce un puntatore all'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del pin di output. |
| [**Inattivo**](cpullpin-inactive.md)               | Arresta il thread di lavoro che esegue il pull dei dati dal pin di output.                     |
| [**Seek**](cpullpin-seek.md)                       | Imposta le posizioni iniziale e di arresto del flusso.                                      |
| Metodi virtuali puri                                | Descrizione                                                                           |
| [**BeginFlush**](cpullpin-beginflush.md)           | Indica al filtro proprietario di scaricare i filtri downstream.                            |
| [**EndFlush**](cpullpin-endflush.md)               | Indica al filtro proprietario di terminare un'operazione di scaricamento.                                   |
| [**EndOfStream**](cpullpin-endofstream.md)         | Chiamato dopo che l'oggetto ha recapitato l'ultimo esempio.                                     |
| [**Onerror**](cpullpin-onerror.md)                 | Chiamato se si verifica un errore durante il flusso.                                           |
| [**Ricevere**](cpullpin-receive.md)                 | Chiamato quando l'oggetto riceve un campione multimediale dal pin di output.                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



 

 




