---
description: 'Metodo CMemAllocator.Alloc: il metodo Alloc alloca memoria per i buffer.'
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Metodo CMemAllocator.Alloc (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93d3f367b0aa69fd2b5782e7cf3c830c30f140389d8611caadc7b70372762625
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813791"
---
# <a name="cmemallocatoralloc-method"></a>Metodo CMemAllocator.Alloc

Il `Alloc` metodo alloca memoria per i buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Operazione completata.<br/>                          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memoria insufficiente.<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | I requisiti del buffer non sono stati impostati.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal [**metodo CBaseAllocator::Commit.**](cbaseallocator-commit.md) Alloca un blocco contiguo di memoria sufficiente per i requisiti del buffer dati nel [**metodo CMemAllocator::SetProperties.**](cmemallocator-setproperties.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




