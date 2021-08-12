---
description: Il metodo SetControlVideoPin imposta il segnaposto usato dal filtro.
ms.assetid: 4346f828-4380-4150-9ecb-74eb690bdcdf
title: Metodo CBaseControlVideo.SetControlVideoPin (Ctlutil.h)
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
ms.openlocfilehash: 6169b5d2ec71148cd868e340c5a2f4e206355044ce55e0905c20787ddb3a263e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660786"
---
# <a name="cbasecontrolvideosetcontrolvideopin-method"></a>Metodo CBaseControlVideo.SetControlVideoPin

Il `SetControlVideoPin` metodo imposta il segnaposto utilizzato dal filtro.

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

Puntatore al pin con cui è sincronizzata l'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

L'interfaccia può essere chiamata solo quando il filtro è stato connesso correttamente. L'oggetto viene passato tramite questo metodo al pin con cui è sincronizzato. nella maggior parte dei casi determinerà se il pin è connesso quando ha un metodo di interfaccia chiamato e restituirà VFW E NOT CONNECTED in caso \_ \_ di \_ errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlVideo**](cbasecontrolvideo.md)
</dt> </dl>

 

 




