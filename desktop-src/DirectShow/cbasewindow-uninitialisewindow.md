---
description: Il metodo UninitialiseWindow rilascia le risorse della finestra.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Metodo CBaseWindow. UninitialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.UninitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ceeadd0ec7a61422f0127c957125caa9a01dcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333325"
---
# <a name="cbasewindowuninitialisewindow-method"></a>CBaseWindow. UninitialiseWindow, metodo

Il `UninitialiseWindow` metodo rilascia le risorse della finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo libera le risorse acquisite dal metodo [**CBaseWindow:: InitialiseWindow**](cbasewindow-initialisewindow.md) . Il metodo [**CBaseWindow::D onewithwindow**](cbasewindow-donewithwindow.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




