---
description: Il metodo DisplayPinInfo traccia una connessione pin durante il debug.
ms.assetid: 3c1aa5ab-7f6b-4518-abf3-b5138f6267ee
title: Metodo CBasePin.DisplayPinInfo (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayPinInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98930ec48d3daa13d6ae463b38ce1ae62d745de9fae65915dcabcedf3cd673aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916471"
---
# <a name="cbasepindisplaypininfo-method"></a>Metodo CBasePin.DisplayPinInfo

Il `DisplayPinInfo` metodo traccia una connessione pin durante il debug.

## <a name="syntax"></a>Sintassi


```C++
void DisplayPinInfo(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntatore al pin ricevente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Nelle build di debug, questo metodo chiama la [**funzione DbgLog**](dbglog.md) per tracciare un tentativo di connessione. Nelle build di vendita al dettaglio questo metodo non esegue alcuna operazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (include Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




