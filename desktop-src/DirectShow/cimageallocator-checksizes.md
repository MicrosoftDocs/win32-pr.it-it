---
description: Il metodo CheckSizes controlla le proprietà dell'allocatore rispetto al tipo di supporto corrente.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Metodo CImageAllocator. CheckSizes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329774"
---
# <a name="cimageallocatorchecksizes-method"></a>CImageAllocator. CheckSizes, metodo

Il `CheckSizes` metodo controlla le proprietà dell'allocatore rispetto al tipo di supporto corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRequest* 
</dt> <dd>

Puntatore a una struttura di [**\_ proprietà dell'allocatore**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che descrive le proprietà dell'allocatore richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                           | Descrizione                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                  | Le proprietà richieste sono compatibili con il tipo di supporto.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Le proprietà richieste non sono compatibili con il tipo di supporto.<br/> |
| <dl> <dt>**VFW \_ E \_ non \_ connesso**</dt> </dl> | Il pin proprietario non è connesso.<br/>                                 |



 

## <a name="remarks"></a>Commenti

Quando il metodo restituisce, se il valore restituito è \_ OK, il membro **cbBuffer** di *pRequest* contiene le dimensioni effettive del buffer. Questo potrebbe essere maggiore della dimensione richiesta, ma non sarà mai minore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




