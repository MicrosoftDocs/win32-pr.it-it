---
description: Implementa un allocatore che supporta l'interfaccia IMemAllocator.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Classe CMemAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb94d5fae92d7494a4ac347591e9d571a7765d2be88072559fd74687eea87e97
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915931"
---
# <a name="cmemallocator-class"></a>Classe CMemAllocator

![Gerarchia di classi cmemallocator](images/filter10.png)

Implementa un allocatore che supporta [**l'interfaccia IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

Questa classe deriva da [**CBaseAllocator.**](cbaseallocator.md) Per altre informazioni sugli allocatori, vedere la documentazione per [**CBaseAllocator**](cbaseallocator.md).



| Variabili membro protette                              | Descrizione                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [**m \_ pBuffer**](cmemallocator-m-pbuffer.md)           | Puntatore al blocco di memoria che contiene i buffer.                   |
| Metodi protetti                                       | Descrizione                                                              |
| [**Gratuito**](cmemallocator-free.md)                      | Metodo segnaposto; chiamato durante un'operazione di decommit.                  |
| [**ReallyFree**](cmemallocator-reallyfree.md)          | Rilascia la memoria per i buffer.                                     |
| [**Alloc**](cmemallocator-alloc.md)                    | Alloca memoria per i buffer.                                        |
| Metodi pubblici                                          | Descrizione                                                              |
| [**CMemAllocator**](cmemallocator-cmemallocator.md)    | Metodo del costruttore.                                                      |
| [**~ CMemAllocator**](cmemallocator--cmemallocator.md) | Metodo del distruttore.                                                       |
| [**CreateInstance**](cmemallocator-createinstance.md)  | Crea una nuova istanza della **classe CMemAllocator.**                   |
| Metodi IMemAllocator                                   | Descrizione                                                              |
| [**SetProperties**](cmemallocator-setproperties.md)    | Specifica il numero di buffer da allocare e la dimensione di ogni buffer. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Specifica di un allocatore personalizzato](providing-a-custom-allocator.md)
</dt> </dl>

 

 




