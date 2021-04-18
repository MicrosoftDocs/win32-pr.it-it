---
description: Il metodo getconnected Recupera il pin connesso a questo pin.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Metodo CBasePin. getconnected (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328847"
---
# <a name="cbasepingetconnected-method"></a>Metodo CBasePin. getconnected

Il `GetConnected` metodo recupera il pin connesso a questo pin.

## <a name="syntax"></a>Sintassi


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.

## <a name="remarks"></a>Commenti

Se il PIN non è connesso, questo metodo restituisce **null**. Chiamare il metodo [**CBasePin:: disconnected**](cbasepin-isconnected.md) per determinare se il PIN è connesso.

Il metodo non chiama **AddRef** sull'interfaccia **Ipin** , pertanto il chiamante non deve rilasciare l'interfaccia.

## <a name="examples"></a>Esempio

Poiché il conteggio dei riferimenti non viene incrementato nel puntatore restituito, è possibile concatenare le chiamate al metodo:


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Questo modello di codifica è molto utile. Tuttavia, come illustrato nell'esempio, è necessario prestare attenzione a non dereferenziare un puntatore **null** quando il PIN è scollegato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter. h (include Streams. h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




