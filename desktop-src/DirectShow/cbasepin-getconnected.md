---
description: Il metodo GetConnected recupera il pin connesso a questo pin.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Metodo CBasePin.GetConnected (Amfilter.h)
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
ms.openlocfilehash: 8bac5bc971f67c7678d2160cadb452995165638db4bb44d2ed1c89b3ab08f882
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526841"
---
# <a name="cbasepingetconnected-method"></a>Metodo CBasePin.GetConnected

Il `GetConnected` metodo recupera il pin connesso a questo pin.

## <a name="syntax"></a>Sintassi


```C++
IPin* GetConnected();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un puntatore all'interfaccia [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) dell'altro pin.

## <a name="remarks"></a>Commenti

Se il pin non è connesso, questo metodo restituisce **NULL.** Chiamare il [**metodo CBasePin::IsConnected**](cbasepin-isconnected.md) per determinare se il pin è connesso.

Il metodo non chiama **AddRef sull'interfaccia** **IPin,** quindi il chiamante non deve rilasciare l'interfaccia.

## <a name="examples"></a>Esempio

Poiché il conteggio dei riferimenti non viene incrementato sul puntatore restituito, è possibile concatenare le chiamate al metodo:


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



Questo modello di codifica è molto pratico. ma, come illustrato nell'esempio, è necessario prestare attenzione a non dereferenziare un **puntatore NULL** quando il pin non è interconnesso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Amfilter.h (includere Flussi.h)</dt> </dl>                                                                                  |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




