---
description: Il metodo PerformanceAlignWindow allinea la posizione della finestra ai limiti DWORD, per ottenere le prestazioni massime.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Metodo CBaseWindow. PerformanceAlignWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PerformanceAlignWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e6e7a54372743d430cd904f47c79414d149cf033
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332587"
---
# <a name="cbasewindowperformancealignwindow-method"></a>CBaseWindow. PerformanceAlignWindow, metodo

Il `PerformanceAlignWindow` Metodo allinea la posizione della finestra ai limiti **DWORD** , per ottenere le prestazioni massime.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo allinea i bordi sinistro e superiore della finestra ai limiti DWORD, che possono migliorare le prestazioni. Se la finestra dispone di un elemento padre, il metodo restituisce \_ OK, ma esegue l'allineamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




