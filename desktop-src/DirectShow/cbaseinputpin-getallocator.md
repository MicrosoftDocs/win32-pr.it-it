---
description: "Il metodo getallocator recupera l'allocatore di memoria proposto da questo pin. Questo metodo implementa il metodo IMemInputPin:: getallocator."
ms.assetid: 07bc77f8-a877-4403-b424-20bda715a818
title: Metodo CBaseInputPin. getallocator (Amfilter. h)
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
ms.openlocfilehash: 098738fc63ba1834b1eefb4b2518e3309db35c43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326065"
---
# <a name="cbaseinputpingetallocator-method"></a>Metodo CBaseInputPin. getallocator

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

Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) dell'allocatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un codice di errore della funzione **CoCreateInstance** .

## <a name="remarks"></a>Commenti

Questo metodo crea un oggetto [**CMemAllocator**](cmemallocator.md) . Eseguire l'override di questo metodo se il filtro usa un allocatore da un pin downstream o un allocatore personalizzato.

Se il metodo ha esito positivo, l'interfaccia **IMemAllocator** ha un conteggio dei riferimenti in attesa. Assicurarsi di rilasciarlo al termine dell'operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




