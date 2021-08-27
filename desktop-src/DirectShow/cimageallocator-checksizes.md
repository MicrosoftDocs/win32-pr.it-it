---
description: Il metodo CheckSizes controlla le proprietà dell'allocatore rispetto al tipo di supporto corrente.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Metodo CImageAllocator.CheckSizes (Winutil.h)
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
ms.openlocfilehash: 070c0cac981f73ea6fa7e3c0ecb620e262f744edd651571be9b592840ad23956
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076231"
---
# <a name="cimageallocatorchecksizes-method"></a>Metodo CImageAllocator.CheckSizes

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

Puntatore a una [**struttura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) che descrive le proprietà dell'allocatore richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                           | Descrizione                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Le proprietà richieste sono compatibili con il tipo di supporto.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Le proprietà richieste non sono compatibili con il tipo di supporto.<br/> |
| <dl> <dt>**VFW \_ E \_ NON \_ CONNESSO**</dt> </dl> | Il pin proprietario non è connesso.<br/>                                 |



 

## <a name="remarks"></a>Commenti

Quando il metodo viene restituito, se il valore restituito è S OK, il membro \_ **cbBuffer** di *pRequest* contiene le dimensioni effettive del buffer. Potrebbe essere maggiore delle dimensioni richieste, ma non sarà mai più piccolo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




