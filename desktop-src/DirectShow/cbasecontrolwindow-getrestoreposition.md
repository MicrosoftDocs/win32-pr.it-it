---
description: Il metodo GetRestorePosition recupera la posizione in cui verrà ripristinata la finestra quando non è ingrandita o ridotta a icona.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Metodo CBaseControlWindow.GetRestorePosition (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetRestorePosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 215b71d731227641df02716dd2b760f7e023bbec0c50bc66ac6d390ed87d002e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757611"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>Metodo CBaseControlWindow.GetRestorePosition

Il metodo recupera la posizione in cui verrà ripristinata la finestra quando non è `GetRestorePosition` ingrandita o ridotta a icona.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRestorePosition(
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

Puntatore al valore della coordinata più a sinistra.

</dd> <dt>

*pTop* 
</dt> <dd>

Puntatore al valore per la parte superiore della finestra.

</dd> <dt>

*pWidth* 
</dt> <dd>

Puntatore al valore per la larghezza della finestra.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntatore al valore per l'altezza della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Corrisponde ai valori restituiti dalla funzione [**CBaseControlWindow::GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) quando la finestra non è ingrandita né ridotta a icona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




