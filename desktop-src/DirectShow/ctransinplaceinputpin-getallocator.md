---
description: "Il metodo getallocator recupera l'allocatore di memoria proposto da questo pin. Questo metodo implementa il metodo IMemInputPin:: getallocator."
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Metodo CTransInPlaceInputPin. getallocator (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326198"
---
# <a name="ctransinplaceinputpingetallocator-method"></a>Metodo CTransInPlaceInputPin. getallocator

Il `GetAllocator` metodo recupera l'allocatore di memoria proposto da questo pin. Questo metodo implementa il metodo [**IMemInputPin:: Getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAllocator* 
</dt> <dd>

Riceve un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . I valori possibili includono quelli mostrati nella tabella seguente.



| Codice restituito                                                                                          | Descrizione                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                 | Esito positivo.<br/>                   |
| <dl> <dt>**\_ \_ \_ allocatore E nessun allocatore**</dt> </dl> | Nessun allocatore disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Se il pin di output del filtro è connesso, questo metodo richiede un allocatore dal pin di input del filtro downstream.

Se il pin di output del filtro non è connesso, questo metodo crea un allocatore temporaneo. Successivamente, quando il pin di output sarà connesso, il filtro riconnetterà il pin di input e rinegozierà l'allocatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




