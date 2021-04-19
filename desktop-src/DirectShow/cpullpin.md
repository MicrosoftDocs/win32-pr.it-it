---
description: La classe CPullPin fornisce supporto per i pin di input che effettuano il pull dei dati attraverso l'interfaccia IAsyncReader.
ms.assetid: 33a6c342-3896-41f8-b32d-01db3eed003e
title: Classe CPullPin (Pullpin. h)
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
ms.openlocfilehash: 3039f97ca7fda43e4ecc6bd4eae05fff2ce90e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331329"
---
# <a name="cpullpin-class"></a>Classe CPullPin

![gerarchia di classi cpullpin](images/pulpin01.png)

La `CPullPin` classe fornisce supporto per i pin di input che effettuano il pull dei dati tramite l'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) . Usare questa classe se si implementa un filtro che usa il modello pull per richiedere i dati dal filtro upstream. Per altre informazioni, vedere flusso di dati nel grafico filtro e modello pull.

Questa classe non deriva da **CBasePin** o implementa l'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) e alcuni nomi di metodo si scontrano con **Ipin**, quindi è consigliabile usarlo come oggetto helper all'interno del PIN. Per usare questa classe, eseguire le operazioni seguenti:

1.  Derivare una classe helper da `CPullPin` e derivare una classe pin di input da **CBasePin**. Dichiarare un'istanza dell' `CPullPin` oggetto come variabile membro della classe pin.
2.  Eseguire l'override del metodo [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) per chiamare [**CPullPin:: Connect**](cpullpin-connect.md). Questo metodo esegue una query sull'altro pin per **IAsyncReader**.
3.  Eseguire l'override del metodo [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) per chiamare [**CPullPin::D Disconnect**](cpullpin-disconnect.md).
4.  Eseguire l'override del metodo [**CBasePin:: Active**](cbasepin-active.md) per chiamare [**CPullPin:: Active**](cpullpin-active.md). Questo metodo avvia un thread di lavoro che estrae gli esempi dal filtro upstream. Quando si connettono i pin, è possibile specificare se si desidera che il thread di lavoro effettui richieste di lettura sincrone o asincrone.
5.  Eseguire l'override del metodo [**CBasePin:: inactive**](cbasepin-inactive.md) per chiamare [**CPullPin:: inactive**](cpullpin-inactive.md). Questo metodo arresta il thread di lavoro.
6.  Implementare il metodo [**CPullPin:: Receive**](cpullpin-receive.md) virtuale pure per elaborare gli esempi in ingresso e distribuirli a valle.
7.  Per impostare le posizioni di arresto e avvio oppure per cercare il flusso, chiamare il metodo [**CPullPin:: Seek**](cpullpin-seek.md) . Questo metodo consente di sospendere il thread di lavoro e di svuotare il grafico del filtro.
8.  Implementare i metodi virtuali pure [**CPullPin:: EndOfStream**](cpullpin-endofstream.md), [**CPullPin:: BeginFlush**](cpullpin-beginflush.md)e [**CPullPin:: EndFlush**](cpullpin-endflush.md) , come descritto nelle osservazioni per tali metodi.
9.  Implementare il metodo [**CPullPin:: OnError**](cpullpin-onerror.md) virtuale pure per gestire gli errori di streaming.



| Variabili membro pubblico                             | Descrizione                                                                           |
|-----------------------------------------------------|---------------------------------------------------------------------------------------|
| [**\_pAlloc m**](cpullpin-m-palloc.md)              | Puntatore all'interfaccia **IMemAllocator** dell'allocatore di memoria.                   |
| Metodi pubblici                                      | Descrizione                                                                           |
| [**Attivo**](cpullpin-active.md)                   | Crea un thread di lavoro che estrae i dati dal pin di output.                          |
| [**AlignDown**](cpullpin-aligndown.md)             | Tronca un valore in un limite di allineamento specificato.                                  |
| [**AlignUp**](cpullpin-alignup.md)                 | Arrotonda un valore fino a un limite di allineamento specificato.                                  |
| [**Connettersi**](cpullpin-connect.md)                 | Completa una connessione al pin di output.                                             |
| [**CPullPin**](cpullpin-cpullpin.md)               | Metodo del costruttore.                                                                   |
| [**~ CPullPin**](cpullpin--cpullpin.md)             | Metodo del distruttore. Virtuale.                                                           |
| [**DecideAllocator**](cpullpin-decideallocator.md) | Negozia un allocatore con il pin di output. Virtuale.                                 |
| [**Disconnetti**](cpullpin-disconnect.md)           | Becco la connessione con il pin di output.                                             |
| [**Duration**](cpullpin-duration.md)               | Recupera la durata del flusso.                                                 |
| [**GetReader**](cpullpin-getreader.md)             | Restituisce un puntatore all'interfaccia [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) del PIN di output. |
| [**Inattivo**](cpullpin-inactive.md)               | Arresta il thread di lavoro che estrae i dati dal pin di output.                     |
| [**Seek**](cpullpin-seek.md)                       | Imposta le posizioni di inizio e di fine del flusso.                                      |
| Metodi virtuali puri                                | Descrizione                                                                           |
| [**BeginFlush**](cpullpin-beginflush.md)           | Informa il filtro proprietario per scaricare i filtri downstream.                            |
| [**EndFlush**](cpullpin-endflush.md)               | Informa il filtro proprietario per terminare un'operazione di svuotamento.                                   |
| [**EndOfStream**](cpullpin-endofstream.md)         | Chiamato dopo che l'oggetto recapita l'ultimo campione.                                     |
| [**OnError**](cpullpin-onerror.md)                 | Viene chiamato se si verifica un errore durante il flusso.                                           |
| [**Ricevere**](cpullpin-receive.md)                 | Chiamato quando l'oggetto riceve un campione multimediale dal pin di output.                   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Pullpin. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



 

 




