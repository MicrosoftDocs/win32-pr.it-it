---
description: La classe CImageAllocator implementa un allocatore che gestisce le bitmap (DIB) indipendenti dal dispositivo GDI. Questa classe deriva dalla classe CBaseAllocator. Crea esempi di supporti che vengono implementati usando la classe CImageSample.
ms.assetid: edda34a5-3916-4a41-9e2f-a19f12df0947
title: Classe CImageAllocator (Winutil. h)
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
ms.openlocfilehash: ea37dfe8cbbc7baf90e6065f0c54af1a60c3284b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325326"
---
# <a name="cimageallocator-class"></a>Classe CImageAllocator

![gerarchia di classi cimageallocator](images/wutil04.png)

La `CImageAllocator` classe implementa un allocatore che gestisce le bitmap (DIB) indipendenti dal dispositivo GDI. Questa classe deriva dalla classe [**CBaseAllocator**](cbaseallocator.md) . Crea esempi di supporti che vengono implementati usando la classe [**CImageSample**](cimagesample.md) .

Un allocatore è condiviso da due pin connessi, ma è sempre di proprietà di uno dei filtri nella connessione. Un filtro che usa `CImageAllocator` deve tenere traccia del fatto che l'allocatore sia stato fornito da solo o dall'altro filtro. Se l'allocatore è stato fornito da solo, il filtro proprietario può basarsi sul fatto che tutti gli esempi di supporti dell'allocatore sono oggetti **CImageSample** . Può quindi usare l'oggetto **CImageSample** per ottenere informazioni su DIB, memorizzato in una struttura [**DIBDATA**](dibdata.md) .

Il filtro proprietario deve chiamare **NotifyMediaType** ogni volta che viene modificato il tipo di supporto.



| Variabili membro protette                                     | Descrizione                                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**\_pFilter m**](cimageallocator-m-pfilter.md)                | Puntatore al filtro proprietario.                                            |
| [**\_pMediaType m**](cimageallocator-m-pmediatype.md)          | Puntatore al tipo di supporto corrente.                                       |
| Metodi protetti                                              | Descrizione                                                              |
| [**Alloc**](cimageallocator-alloc.md)                         | Alloca memoria per i buffer.                                        |
| [**CheckSizes**](cimageallocator-checksizes.md)               | Verifica le proprietà dell'allocatore rispetto al tipo di supporto corrente.              |
| [**CreateDIB**](cimageallocator-createdib.md)                 | Crea una DIB.                                                           |
| [**CreateImageSample**](cimageallocator-createimagesample.md) | Crea un esempio di supporto. Virtuale.                                         |
| [**Gratuito**](cimageallocator-free.md)                           | Rilascia tutta la memoria del buffer.                                       |
| Metodi pubblici                                                 | Descrizione                                                              |
| [**CImageAllocator**](cimageallocator-cimageallocator.md)     | Metodo del costruttore.                                                      |
| [**NotifyMediaType**](cimageallocator-notifymediatype.md)     | Informa l'oggetto del tipo di supporto corrente.                            |
| Metodi IMemAllocator                                          | Descrizione                                                              |
| [**SetProperties**](cimageallocator-setproperties.md)         | Specifica il numero di buffer da allocare e le dimensioni di ogni buffer. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




