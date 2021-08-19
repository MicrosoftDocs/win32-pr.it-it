---
description: La classe CImageAllocator implementa un allocatore che gestisce bitmap GDI indipendenti dal dispositivo (DIB). Questa classe deriva dalla classe CBaseAllocator. Crea esempi di supporti implementati usando la classe CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Classe CImageAllocator (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 383b9c2ca992db66e7bf397e42dcb8aaaa4bdb66251ddfd67f4b5175d87058aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402584"
---
# <a name="cimageallocator-class"></a>Classe CImageAllocator

![Gerarchia di classi cimageallocator](images/wutil04.png)

La `CImageAllocator` classe implementa un allocatore che gestisce bitmap GDI indipendenti dal dispositivo (DIB). Questa classe deriva dalla [**classe CBaseAllocator.**](cbaseallocator.md) Crea esempi di supporti implementati usando la [**classe CImageSample.**](cimagesample.md)

Un allocatore è condiviso da due pin connessi, ma è sempre di proprietà di uno dei filtri nella connessione. Un filtro che usa deve tenere traccia se l'allocatore è stato fornito da solo `CImageAllocator` o dall'altro filtro. Se l'allocatore è stato fornito da solo, il filtro proprietario può basarsi sul fatto che tutti i campioni multimediali dell'allocatore sono **oggetti CImageSample.** Può quindi usare **l'oggetto CImageSample** per ottenere informazioni sulla dib, archiviata in una [**struttura DIBDATA.**](dibdata.md)

Il filtro proprietario deve chiamare **NotifyMediaType** ogni volta che il tipo di supporto cambia.



| Variabili membro protette                                     | Descrizione                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pFilter**](cimageallocator-m-pfilter.md)                | Puntatore al filtro proprietario.                                            |
| [**m \_ pMediaType**](cimageallocator-m-pmediatype.md)          | Puntatore al tipo di supporto corrente.                                       |
| Metodi protetti                                              | Descrizione                                                              |
| [**Alloc**](cimageallocator-alloc.md)                         | Alloca memoria per i buffer.                                        |
| [**CheckSizes**](cimageallocator-checksizes.md)               | Controlla le proprietà dell'allocatore rispetto al tipo di supporto corrente.              |
| [**CreateDIB**](cimageallocator-createdib.md)                 | Crea un dib.                                                           |
| [**CreateImageSample**](cimageallocator-createimagesample.md) | Crea un esempio di supporto. Virtuale.                                         |
| [**Gratuito**](cimageallocator-free.md)                           | Rilascia tutta la memoria del buffer.                                       |
| Metodi pubblici                                                 | Descrizione                                                              |
| [**CImageAllocator**](cimageallocator-cimageallocator.md)     | Metodo del costruttore.                                                      |
| [**NotifyMediaType**](cimageallocator-notifymediatype.md)     | Informa l'oggetto del tipo di supporto corrente.                            |
| Metodi di IMemAllocator                                          | Descrizione                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | Specifica il numero di buffer da allocare e le dimensioni di ogni buffer. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




