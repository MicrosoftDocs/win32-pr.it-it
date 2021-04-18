---
description: Il metodo DoCreateWindow crea la finestra.
ms.assetid: bbe38a71-bbf7-4380-96a3-074b992a1d1e
title: Metodo CBaseWindow.DoCreateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoCreateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 76bea1523f48a6e22a3c2d9370fa32bcea022621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325340"
---
# <a name="cbasewindowdocreatewindow-method"></a>Metodo reateWindow CBaseWindow.DoC

Il `DoCreateWindow` metodo crea la finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT DoCreateWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se ha esito positivo o un valore **HRESULT** che indica la ragione dell'errore.

## <a name="remarks"></a>Commenti

Il metodo [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) chiama questo metodo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




