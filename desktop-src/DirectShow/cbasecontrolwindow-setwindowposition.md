---
description: Il metodo SetWindowPosition imposta la posizione della finestra sul desktop.
ms.assetid: 1c2706dd-d67c-41c7-b672-3c040f37bc41
title: Metodo CBaseControlWindow.SetWindowPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.SetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2734c93d1a3d3d3ea29e037d1bf85baacd5358a69f08d1517012c3eb250ab8ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635460"
---
# <a name="cbasecontrolwindowsetwindowposition-method"></a>Metodo CBaseControlWindow.SetWindowPosition

Il `SetWindowPosition` metodo imposta la posizione della finestra sul desktop.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetWindowPosition(
   long Left,
   long Top,
   long Width,
   long Height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Sinistra* 
</dt> <dd>

Nuova coordinata sinistra.

</dd> <dt>

*Top* 
</dt> <dd>

Nuova coordinata superiore.

</dd> <dt>

*Larghezza* 
</dt> <dd>

Larghezza della finestra.

</dd> <dt>

*Altezza* 
</dt> <dd>

Altezza della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




