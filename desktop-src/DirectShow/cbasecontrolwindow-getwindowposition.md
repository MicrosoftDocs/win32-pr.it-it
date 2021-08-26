---
description: Il metodo GetWindowPosition recupera le coordinate correnti per la finestra.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Metodo CBaseControlWindow.GetWindowPosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetWindowPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6d576f065e807c2af47621d43940d7e48c54f36f0617d20590953a5e83ab2fc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966731"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>Metodo CBaseControlWindow.GetWindowPosition

Il `GetWindowPosition` metodo recupera le coordinate correnti per la finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetWindowPosition(
   long *pLeft,
   long *pTop,
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pLeft* 
</dt> <dd>

Puntatore alla coordinata sinistra, in coordinate dello schermo.

</dd> <dt>

*pTop* 
</dt> <dd>

Puntatore alla coordinata superiore, in coordinate dello schermo.

</dd> <dt>

*pWidth* 
</dt> <dd>

Puntatore alla larghezza della finestra, in coordinate dello schermo.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntatore all'altezza della finestra, in coordinate dello schermo.

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

 

 




