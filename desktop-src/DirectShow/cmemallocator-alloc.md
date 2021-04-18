---
description: Il metodo Alloc alloca memoria per i buffer.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Metodo CMemAllocator. Alloc (Amfilter. h)
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
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327445"
---
# <a name="cmemallocatoralloc-method"></a>CMemAllocator. Alloc, metodo

Il `Alloc` metodo alloca memoria per i buffer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                                       | Descrizione                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>              | Esito positivo.<br/>                          |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>     | Memoria insufficiente.<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | I requisiti del buffer non sono stati impostati.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo viene chiamato dal metodo [**CBaseAllocator:: commit**](cbaseallocator-commit.md) . Alloca un blocco di memoria contiguo sufficiente per i requisiti del buffer specificati nel metodo [**CMemAllocator:: seproperties**](cmemallocator-setproperties.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




