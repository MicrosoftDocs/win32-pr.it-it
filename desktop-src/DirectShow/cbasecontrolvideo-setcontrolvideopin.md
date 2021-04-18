---
description: Il metodo SetControlVideoPin imposta il PIN utilizzato dal filtro.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Metodo CBaseControlVideo. SetControlVideoPin (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetControlVideoPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4cf47469800a4d1ecd8abe373d6f3c1fd53ece5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325398"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a>CBaseControlVideo. SetControlVideoPin, metodo

Il `SetControlVideoPin` metodo imposta il PIN utilizzato dal filtro.

## <a name="syntax"></a>Sintassi


```C++
void SetControlVideoPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* 
</dt> <dd>

Puntatore al pin con il quale viene sincronizzata l'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'interfaccia può essere chiamata solo quando il filtro è stato connesso correttamente. L'oggetto viene passato tramite questo metodo al pin con il quale è sincronizzato; nella maggior parte dei casi determinerà se il PIN è connesso quando dispone di un metodo di interfaccia denominato e restituirà VFW \_ e \_ non sarà connesso in caso di \_ errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




