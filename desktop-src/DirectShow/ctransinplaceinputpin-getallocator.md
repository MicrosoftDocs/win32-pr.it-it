---
description: "Metodo CTransInPlaceInputPin.GetAllocator: il metodo GetAllocator recupera l'allocatore di memoria proposto da questo pin. Questo metodo implementa il metodo IMemInputPin::GetAllocator."
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Metodo CTransInPlaceInputPin.GetAllocator (Transip.h)
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
ms.openlocfilehash: c3c90587cbd0a9cc9b0abed834db68de3edac6f73d98dac3c8bb283e77f978fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654852"
---
# <a name="ctransinplaceinputpingetallocator-method"></a>Metodo CTransInPlaceInputPin.GetAllocator

Il `GetAllocator` metodo recupera l'allocatore di memoria proposto da questo pin. Questo metodo implementa il [**metodo IMemInputPin::GetAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)

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

Restituisce un **valore HRESULT.** I valori possibili includono quelli illustrati nella tabella seguente.



| Codice restituito                                                                                          | Descrizione                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                 | Operazione completata.<br/>                   |
| <dl> <dt>**VFW \_ E \_ NO \_ ALLOCATOR**</dt> </dl> | Nessun allocatore disponibile.<br/> |



 

## <a name="remarks"></a>Commenti

Se il pin di output del filtro è connesso, questo metodo richiede un allocatore dal pin di input del filtro downstream.

Se il pin di output del filtro non è connesso, questo metodo crea un allocatore temporaneo. Successivamente, quando il pin di output è connesso, il filtro riconnetterà il pin di input e rinegozia l'allocatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Transip.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




