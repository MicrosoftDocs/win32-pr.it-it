---
description: "Il metodo GetAllocatorRequirements recupera le proprietà dell'allocatore richieste dal pin. Questo metodo implementa il metodo IMemInputPin:: GetAllocatorRequirements."
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Metodo CTransInPlaceInputPin. GetAllocatorRequirements (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfa176cd5da0317821996593e19bb90396e82224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330835"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a>CTransInPlaceInputPin. GetAllocatorRequirements, metodo

Il `GetAllocatorRequirements` metodo recupera le proprietà dell'allocatore richieste dal pin. Questo metodo implementa il metodo [**IMemInputPin:: GetAllocatorRequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) .

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

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                               | Descrizione                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>      | Operazione riuscita<br/>                                                                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Il pin di output non è connesso oppure il pin di input downstream non supporta il metodo.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl> | Argomento puntatore **null**<br/>                                                                 |



 

## <a name="remarks"></a>Commenti

Se il pin di output è connesso, questo metodo passa la chiamata al pin di input downstream. In caso contrario, restituisce E \_ NOTIMPL.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




