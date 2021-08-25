---
description: Il metodo SetControlWindowPin imposta il pin con cui eseguire la sincronizzazione.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Metodo CBaseControlWindow.SetControlWindowPin (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetControlWindowPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9ab7cbb5d199b0908c2eb51ffb5a70eda7eb1336bd66a1645daad61b3202d69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056711"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>Metodo CBaseControlWindow.SetControlWindowPin

Il `SetControlWindowPin` metodo imposta il pin con cui eseguire la sincronizzazione.

## <a name="syntax"></a>Sintassi


```C++
void SetControlWindowPin(
   CBasePin *pPin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPin* 
</dt> <dd>

Puntatore al pin con cui viene sincronizzata l'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questa funzione membro imposta la variabile \_ membro m pPin uguale al parametro pPin. Come descritto nel costruttore , l'interfaccia può essere chiamata solo quando il filtro è stato connesso correttamente. L'oggetto viene passato tramite questa funzione membro al pin con cui deve essere sincronizzato. Nella maggior parte dei casi, determinerà se il pin è connesso ogni volta che ha un metodo di interfaccia denominato e restituirà VFW E NOT CONNECTED in caso \_ \_ di \_ errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




