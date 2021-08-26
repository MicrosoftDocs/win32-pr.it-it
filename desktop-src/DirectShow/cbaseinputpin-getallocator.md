---
description: "Metodo CBaseInputPin.GetAllocator: il metodo GetAllocator recupera l'allocatore di memoria proposto da questo pin. Questo metodo implementa il metodo IMemInputPin::GetAllocator."
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Metodo CBaseInputPin.GetAllocator (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 119f3ffaa5863584b55210306b38b011c758f9bab0febac47547bdfe469b5ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056341"
---
# <a name="cbaseinputpingetallocator-method"></a>Metodo CBaseInputPin.GetAllocator

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

Indirizzo di una variabile che riceve un puntatore [**all'interfaccia IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S OK in caso di esito positivo o un \_ codice di errore dalla funzione **CoCreateInstance.**

## <a name="remarks"></a>Commenti

Questo metodo crea un [**oggetto CMemAllocator.**](cmemallocator.md) Eseguire l'override di questo metodo se il filtro usa un allocatore da un pin downstream o un allocatore personalizzato.

Se il metodo ha esito positivo, **l'interfaccia IMemAllocator** ha un conteggio dei riferimenti in sospeso. Al termine, assicurarsi di rilasciarlo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




