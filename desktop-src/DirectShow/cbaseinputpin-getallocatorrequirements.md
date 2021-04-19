---
description: Il metodo GetAllocatorRequirements recupera le proprietà dell'allocatore richieste dal pin di input.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Metodo CBaseInputPin. GetAllocatorRequirements (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326064"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>CBaseInputPin. GetAllocatorRequirements, metodo

Il `GetAllocatorRequirements` metodo recupera le proprietà dell'allocatore richieste dal pin di input.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProps* 
</dt> <dd>

Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , compilata con i requisiti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

Quando un pin di output Inizializza un allocatore di memoria, può chiamare questo metodo per determinare se il pin di input presenta requisiti di buffer. Per ulteriori informazioni, vedere [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).

L'implementazione di questo metodo è facoltativa. Se il filtro ha requisiti di allineamento o prefisso specifici, eseguire l'override di questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




