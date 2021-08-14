---
description: Il metodo GetOwnerWindow recupera l'handle di finestra proprietario, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Metodo CBaseControlWindow.GetOwnerWindow (Ctlutil.h)
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
ms.openlocfilehash: 0cdb3073d1dd8055986b905d6e8f50967a304e5f294b0ffcaeddcd50d8c0ee33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432511"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>Metodo CBaseControlWindow.GetOwnerWindow

Il `GetOwnerWindow` metodo recupera l'handle di finestra proprietario, **m \_ hwndOwner.**

## <a name="syntax"></a>Sintassi


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce la finestra proprietaria.

## <a name="remarks"></a>Commenti

Recupera la finestra proprietaria senza chiamare il metodo di interfaccia . Usare questa funzione membro anziché [**CBaseControlWindow::get \_ Owner**](cbasecontrolwindow-get-owner.md), a meno che non venga chiamato esternamente tramite il metodo [**IVideoWindow::get \_ Owner.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




