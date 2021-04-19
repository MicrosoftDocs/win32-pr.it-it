---
description: Il \_ metodo Put WindowState imposta lo stato della finestra.
ms.assetid: 0d22fa84-17bc-4228-b86e-d31857156802
title: Metodo CBaseControlWindow.put_WindowState (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_WindowState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1944e9bd39816cd1f022296b69fdac60d0779f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333369"
---
# <a name="cbasecontrolwindowput_windowstate-method"></a>CBaseControlWindow. put \_ WindowState (metodo)

Il `put_WindowState` metodo imposta lo stato della finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_WindowState(
   long WindowState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*WindowState* 
</dt> <dd>

Nuovo stato della finestra.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro accetta gli stessi parametri della funzione **ShowWindow** di Microsoft Win32 (ad esempio, WS \_ SHOWNORMAL, WS \_ SHOWMINNOACTIVATE e WS \_ SHOWMAXIMIZED).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




