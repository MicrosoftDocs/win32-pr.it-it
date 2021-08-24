---
description: Il metodo InitAllocator crea un allocatore di memoria.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.Inimetodo tAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce1e8f8097ca88d0434f79c20e855d8b61798b5a1b0e32b6a38077e4c7aa1271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652461"
---
# <a name="cbaseoutputpininitallocator-method"></a>CBaseOutputPin.Inimetodo tAllocator

Il `InitAllocator` metodo crea un allocatore di memoria.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppAlloc* 
</dt> <dd>

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK in caso di esito positivo o un codice di errore dalla funzione **CoCreateInstance.**

## <a name="remarks"></a>Commenti

Se il pin di input non fornisce un allocatore di memoria, il metodo [**CBaseOutputPin::D ecideAllocator**](cbaseoutputpin-decideallocator.md) chiama questo metodo per creare un allocatore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




