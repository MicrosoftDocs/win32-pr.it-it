---
description: Puntatore all'allocatore che ha creato questo esempio.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: Membro CMediaSample::m_pAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 646c6fb7f8236aca87b5aebd1d30fd67750d960da4445d45bf45d8b601320274
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118156543"
---
# <a name="cmediasamplem_pallocator-member"></a>Membro CMediaSample::m \_ pAllocator

Puntatore all'allocatore che ha creato questo esempio.

## <a name="syntax"></a>Sintassi


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Osservazioni

Anche se l'esempio mantiene un puntatore all'allocatore, non contiene un conteggio dei riferimenti. Al contrario, l'allocatore incrementa il proprio conteggio dei riferimenti nel metodo [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) e si rilascia nel [**metodo IMemAllocator::ReleaseBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) Ciò garantisce che l'allocatore sarà disponibile purché l'esempio sia utilizzato da un altro oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




