---
description: Il metodo OnSize gestisce \_ i messaggi di dimensioni WM.
ms.assetid: 21d867a4-4321-478a-9beb-5d3053569369
title: Metodo CBaseWindow. OnSize (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9020510030d3b3d4b30e066adfe67367618fb3d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325760"
---
# <a name="cbasewindowonsize-method"></a>Metodo CBaseWindow. OnSize

Il `OnSize` metodo gestisce \_ i messaggi di dimensioni WM.

## <a name="syntax"></a>Sintassi


```C++
virtual BOOL OnSize(
   LONG Width,
   LONG Height
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Larghezza* 
</dt> <dd>

Larghezza dell'area client in pixel.

</dd> <dt>

*Altezza* 
</dt> <dd>

Altezza dell'area client in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true**.

## <a name="remarks"></a>Commenti

Questo metodo archivia la nuova larghezza e altezza. Per recuperare questi valori, chiamare i metodi [**CBaseWindow:: GetWindowHeight**](cbasewindow-getwindowheight.md) e [**CBaseWindow:: GetWindowWidth**](cbasewindow-getwindowwidth.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




