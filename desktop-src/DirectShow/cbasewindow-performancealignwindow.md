---
description: Il metodo PerformanceAlignWindow allinea la posizione della finestra ai limiti DWORD, per ottenere prestazioni ottimali.
ms.assetid: e28950bc-2510-45b9-9c9c-c2a9dbc3dc02
title: Metodo CBaseWindow.PerformanceAlignWindow (Winutil.h)
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
ms.openlocfilehash: a3c077b6cf00f61565124f3d79ad905f6d34a3d8da50d58396e2df1bd35b0d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016469"
---
# <a name="cbasewindowperformancealignwindow-method"></a>Metodo CBaseWindow.PerformanceAlignWindow

Il `PerformanceAlignWindow` metodo allinea la posizione della finestra ai limiti **DWORD,** per ottenere prestazioni ottimali.

## <a name="syntax"></a>Sintassi


```C++
HRESULT PerformanceAlignWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo allinea i bordi sinistro e superiore della finestra ai limiti DWORD, migliorando le prestazioni. Se la finestra ha un elemento padre, il metodo restituisce S \_ OK, ma esegue l'allineamento.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




