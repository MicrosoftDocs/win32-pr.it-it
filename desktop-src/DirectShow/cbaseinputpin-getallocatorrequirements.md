---
description: Il metodo GetAllocatorRequirements recupera le proprietà dell'allocatore richieste dal pin di input.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Metodo CBaseInputPin.GetAllocatorRequirements (Amfilter.h)
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
ms.openlocfilehash: 57b085cd82c45fd78ddaa4794084cba775e1c80cd8b9e3b8df4c9680379ba462
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586371"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a>Metodo CBaseInputPin.GetAllocatorRequirements

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

Puntatore a [**una struttura \_ ALLOCATOR PROPERTIES,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che viene compilata con i requisiti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ NOTIMPL.

## <a name="remarks"></a>Commenti

Quando un pin di output inizializza un allocatore di memoria, può chiamare questo metodo per determinare se il pin di input presenta requisiti di buffer. Per altre informazioni, vedere [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md).

L'implementazione di questo metodo è facoltativa. Se il filtro ha requisiti di allineamento o prefisso specifici, eseguire l'override di questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




