---
description: Il metodo GetWindowPosition recupera le coordinate correnti per la finestra.
ms.assetid: a2f46a87-b2cd-450f-8d2b-0f8695432fda
title: Metodo CBaseControlWindow. GetWindowPosition (Ctlutil. h)
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
ms.openlocfilehash: af2b1bdb8b2c839644e8c0629e3e272c123d3c21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328085"
---
# <a name="cbasecontrolwindowgetwindowposition-method"></a>CBaseControlWindow. GetWindowPosition, metodo

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

Puntatore alla coordinata sinistra, espressa in coordinate dello schermo.

</dd> <dt>

*pTop* 
</dt> <dd>

Puntatore alla coordinata superiore, espressa in coordinate dello schermo.

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

Restituisce un valore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




