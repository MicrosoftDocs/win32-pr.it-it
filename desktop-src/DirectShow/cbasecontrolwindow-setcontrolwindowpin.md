---
description: Il metodo SetControlWindowPin imposta il pin con cui eseguire la sincronizzazione.
ms.assetid: 6373c046-5448-4159-88b9-9b2babdb938b
title: Metodo CBaseControlWindow. SetControlWindowPin (Ctlutil. h)
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
ms.openlocfilehash: c1aa3d4960799c2286e17709258ea90b76332bc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333363"
---
# <a name="cbasecontrolwindowsetcontrolwindowpin-method"></a>CBaseControlWindow. SetControlWindowPin, metodo

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

Puntatore al pin con il quale viene sincronizzata l'interfaccia.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Nessun valore restituito.

## <a name="remarks"></a>Commenti

Questa funzione membro imposta la \_ variabile membro pPin m uguale al parametro pPin. Come descritto nel costruttore, l'interfaccia può essere chiamata solo quando il filtro è stato connesso correttamente. L'oggetto viene passato tramite questa funzione membro al pin con il quale deve essere sincronizzato; nella maggior parte dei casi, determina se il PIN è connesso ogni volta che è presente un metodo di interfaccia denominato e restituisce VFW \_ e \_ non \_ connesso in caso di errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




