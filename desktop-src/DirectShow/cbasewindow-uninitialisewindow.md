---
description: Il metodo UninitialiseWindow rilascia le risorse della finestra.
ms.assetid: 8c5bb0c1-1d92-4025-bbbd-1e57ddde4456
title: Metodo CBaseWindow.UninitialiseWindow (Winutil.h)
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
ms.openlocfilehash: c275e4d683bcc698c8f04c5a85017b081b6aad17f93c91d66e0a75f2da88692e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657493"
---
# <a name="cbasewindowuninitialisewindow-method"></a>Metodo CBaseWindow.UninitialiseWindow

Il `UninitialiseWindow` metodo rilascia le risorse della finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT UninitialiseWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK.

## <a name="remarks"></a>Commenti

Questo metodo libera le risorse acquisite dal metodo [**CBaseWindow::InitialiseWindow.**](cbasewindow-initialisewindow.md) Il [**metodo CBaseWindow::D oneWithWindow**](cbasewindow-donewithwindow.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




