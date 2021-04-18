---
description: La classe CBaseAllocator è una classe di base astratta che implementa un allocatore. Gli allocatori espongono l'interfaccia IMemAllocator.
ms.assetid: 3c9003d8-f15c-4e85-9712-9aaa87dffdf3
title: Classe CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 068dd45ee3ffac5c3b915c3b0cdd8bc87756377e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327586"
---
# <a name="cbaseallocator-class"></a>Classe CBaseAllocator

![gerarchia di classi cbaseallocator](images/filter10.png)

La classe **CBaseAllocator** è una classe di base astratta che implementa un allocatore. Gli allocatori espongono l'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .

Un *allocatore* è un oggetto che alloca buffer di memoria. L'allocatore gestisce un elenco di buffer disponibili. Quando un client (in genere un filtro) richiede un buffer, l'allocatore ne recupera uno dall'elenco. Il client riempie il buffer con i dati e potrebbe passare il buffer a un altro oggetto. Infine, il buffer viene rilasciato e l'allocatore lo restituisce all'elenco dei buffer disponibili.

Ogni buffer è incapsulato da un oggetto denominato *esempio multimediale*. Gli esempi di supporti consentono di creare pacchetti di puntatori a blocchi di memoria all'interno del Framework Component Object Model (COM). Gli esempi di supporti espongono l'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) e vengono implementati usando la classe [**CMediaSample**](cmediasample.md) . Un esempio multimediale contiene un puntatore al buffer associato, a cui è possibile accedere chiamando il metodo [**IMediaSample:: Getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) . Per ulteriori informazioni, vedere [esempi e allocatori](samples-and-allocators.md).

Per usare questa classe, seguire questa procedura:

1.  Chiamare il metodo [**CBaseAllocator:: seproperties**](cbaseallocator-setproperties.md) per specificare i requisiti del buffer, inclusi il numero di buffer e le dimensioni di ogni buffer.
2.  Chiamare il metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) per allocare i buffer.
3.  Chiamare il metodo [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) per recuperare gli esempi di supporti. Questo metodo si blocca fino a quando non viene reso disponibile l'esempio successivo.
4.  Al termine di ogni esempio, chiamare il metodo **IUnknown:: Release** nell'esempio. L'esempio non viene eliminato quando il relativo conteggio dei riferimenti raggiunge zero. Al contrario, l'esempio restituisce l'elenco di disponibilità dell'allocatore.
5.  Al termine dell'utilizzo dell'allocatore, chiamare il metodo [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) per liberare la memoria per i buffer.

Il metodo [**commit**](cbaseallocator-commit.md) chiama il metodo virtuale [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md), che alloca la memoria per i buffer. Il metodo [**decommit**](cbaseallocator-decommit.md) chiama il metodo virtuale pure [**CBaseAllocator:: Free**](cbaseallocator-free.md), che libera la memoria. Le classi derivate devono eseguire l'override di questi due metodi.

La classe base [**CMemAllocator**](cmemallocator.md) deriva da **CBaseAllocator**. Le classi base del filtro usano la classe **CMemAllocator** .



| Variabili membro protette                                                   | Descrizione                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**\_lFree m**](cbaseallocator-m-lfree.md)                                   | Puntatore a un elenco di esempi di supporti (gratuiti) disponibili.                                       |
| [**\_hSem m**](cbaseallocator-m-hsem.md)                                     | Semaforo segnalato quando un campione diventa disponibile.                                |
| [**\_lWaiting m**](cbaseallocator-m-lwaiting.md)                             | Numero di thread in attesa di campioni.                                                      |
| [**\_lCount m**](cbaseallocator-m-lcount.md)                                 | Numero di buffer da fornire.                                                              |
| [**\_lAllocated m**](cbaseallocator-m-lallocated.md)                         | Numero di buffer attualmente allocati.                                                     |
| [**\_lSize m**](cbaseallocator-m-lsize.md)                                   | Dimensioni di ogni buffer.                                                                       |
| [**\_lAlignment m**](cbaseallocator-m-lalignment.md)                         | Allineamento di ogni buffer.                                                                  |
| [**\_lPrefix m**](cbaseallocator-m-lprefix.md)                               | Prefisso di ogni buffer.                                                                     |
| [**\_bChanged m**](cbaseallocator-m-bchanged.md)                             | Flag che indica se i requisiti del buffer sono stati modificati.                              |
| [**\_bCommitted m**](cbaseallocator-m-bcommitted.md)                         | Flag che indica se è stato eseguito il commit dell'allocatore.                                  |
| [**\_bDecommitInProgress m**](cbaseallocator-m-bdecommitinprogress.md)       | Flag che indica se un'operazione di decommit è in corso.                               |
| [**\_pNotify m**](cbaseallocator-m-pnotify.md)                               | Puntatore a un'interfaccia di callback, che viene chiamato quando vengono rilasciati gli esempi.                |
| [**\_fEnableReleaseCallback m**](cbaseallocator-m-fenablereleasecallback.md) | Flag che indica se il callback di rilascio è abilitato.                                   |
| Metodi protetti                                                            | Descrizione                                                                                |
| [**Alloc**](cbaseallocator-alloc.md)                                        | Alloca memoria per i buffer. Virtuale.                                                 |
| Metodi pubblici                                                               | Descrizione                                                                                |
| [**CBaseAllocator**](cbaseallocator-cbaseallocator.md)                      | Metodo del costruttore.                                                                        |
| [**~ CBaseAllocator**](cbaseallocator--cbaseallocator.md)                   | Metodo del distruttore.                                                                         |
| [**Invia notifica**](cbaseallocator-setnotify.md)                                | Obsoleta.                                                                                  |
| [**GetFreeCount**](cbaseallocator-getfreecount.md)                          | Recupera il numero di campioni multimediali che non sono in uso.                                 |
| [**NotifySample**](cbaseallocator-notifysample.md)                          | Rilascia tutti i thread in attesa di esempi.                                         |
| [**In attesa**](cbaseallocator-setwaiting.md)                              | Incrementa il numero di thread in attesa.                                                   |
| Metodi virtuali puri                                                         | Descrizione                                                                                |
| [**Libero**](cbaseallocator-free.md)                                          | Rilascia tutta la memoria del buffer.                                                         |
| Metodi IMemAllocator                                                        | Descrizione                                                                                |
| [**SetProperties**](cbaseallocator-setproperties.md)                        | Specifica il numero di buffer da allocare e le dimensioni di ogni buffer.                   |
| [**GetProperties**](cbaseallocator-getproperties.md)                        | Recupera il numero di buffer che l'allocatore creerà e le proprietà del buffer. |
| [**Commit**](cbaseallocator-commit.md)                                      | Alloca la memoria per i buffer.                                                      |
| [**Liberare**](cbaseallocator-decommit.md)                                  | Decommit dei buffer.                                                                     |
| [**GetBuffer**](cbaseallocator-getbuffer.md)                                | Recupera un esempio multimediale contenente un buffer.                                           |
| [**ReleaseBuffer**](cbaseallocator-releasebuffer.md)                        | Restituisce un esempio di supporto all'elenco di esempi di supporti disponibili.                                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Fornire un allocatore personalizzato](providing-a-custom-allocator.md)
</dt> </dl>

 

 




