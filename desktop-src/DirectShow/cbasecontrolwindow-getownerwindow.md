---
description: Il Metodo GetOwnerWindow recupera l'handle della finestra proprietaria, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Metodo CBaseControlWindow. GetOwnerWindow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e4d3811f85abd68bcd7d625dce0e9e8963be39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328090"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>CBaseControlWindow. GetOwnerWindow, metodo

Il `GetOwnerWindow` metodo recupera l'handle della finestra proprietaria, **m \_ hwndOwner**.

## <a name="syntax"></a>Sintassi


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la finestra proprietaria.

## <a name="remarks"></a>Commenti

Recupera la finestra proprietaria senza chiamare il metodo di interfaccia. Usare questa funzione membro invece di [**CBaseControlWindow:: Get \_ owner**](cbasecontrolwindow-get-owner.md), a meno che non si chiami esternamente tramite il metodo [**IVideoWindow:: Get \_ owner**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




