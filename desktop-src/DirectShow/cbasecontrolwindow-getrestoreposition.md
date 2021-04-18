---
description: Il metodo GetRestorePosition recupera la posizione in cui la finestra verrà ripristinata quando non è ingrandita o ridotta a icona.
ms.assetid: 5f129be3-c4d8-4583-bbc8-870e0bcafd80
title: Metodo CBaseControlWindow. GetRestorePosition (Ctlutil. h)
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
ms.openlocfilehash: f922a97f69f4dae03d4e61a54bd99c52d69a984a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328086"
---
# <a name="cbasecontrolwindowgetrestoreposition-method"></a>CBaseControlWindow. GetRestorePosition, metodo

Il `GetRestorePosition` metodo recupera la posizione in cui la finestra verrà ripristinata quando non è ingrandita o ridotta a icona.

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

Puntatore al valore per la coordinata più a sinistra.

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

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Equivale ai valori restituiti dalla funzione [**CBaseControlWindow:: GetWindowPosition**](cbasecontrolwindow-getwindowposition.md) quando la finestra non è né ingrandita né ridotta a icona.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




