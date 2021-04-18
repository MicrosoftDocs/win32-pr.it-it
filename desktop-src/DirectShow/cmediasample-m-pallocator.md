---
description: Puntatore all'allocatore che ha creato l'esempio.
ms.assetid: b4faccec-9124-4ae6-8662-ac5eb017328a
title: 'Membro CMediaSample:: m_pAllocator (Amfilter. h)'
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
ms.openlocfilehash: ac2943c08b881badd8e15ea0633952ccc973a534
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324933"
---
# <a name="cmediasamplem_pallocator-member"></a>Membro pAllocator di CMediaSample:: m \_

Puntatore all'allocatore che ha creato l'esempio.

## <a name="syntax"></a>Sintassi


```C++
CBaseAllocator *m_pAllocator;
```



## <a name="remarks"></a>Osservazioni

Sebbene nell'esempio venga mantenuto un puntatore all'allocatore, non viene mantenuto un conteggio dei riferimenti. Al contrario, l'allocatore incrementa il proprio conteggio dei riferimenti nel metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) e rilascia se stesso nel metodo [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) . Ciò garantisce che l'allocatore sarà disponibile purché un altro oggetto stia usando l'esempio.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMediaSample**](cmediasample.md)
</dt> </dl>

 

 




