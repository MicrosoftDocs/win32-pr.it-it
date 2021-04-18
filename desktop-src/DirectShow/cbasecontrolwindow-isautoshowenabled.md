---
description: Il metodo IsAutoShowEnabled recupera informazioni sull'eventuale visualizzazione automatica della finestra video quando il filtro di rendering viene sospeso o eseguito.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Metodo CBaseControlWindow. IsAutoShowEnabled (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329264"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>CBaseControlWindow. IsAutoShowEnabled, metodo

Il `IsAutoShowEnabled` metodo recupera informazioni sull'eventuale visualizzazione automatica della finestra video quando il filtro di rendering viene sospeso o eseguito.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **true** se il **membro \_ bAutoShow m** è impostato su 1 o su **false** se è impostato su 0.

## <a name="remarks"></a>Commenti

Se il **membro \_ bAutoShow m** è impostato su 1 in una finestra video nascosta, la finestra diventa visibile quando il filtro viene sospeso o eseguito. Se questo membro è impostato su 0, la finestra viene visualizzata solo se si usa la funzione membro [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con i parametri appropriati.

Questa funzione membro recupera l'impostazione del membro **\_ bAutoShow di m** e ha lo stesso risultato dell'utilizzo del metodo [**IVideoWindow:: Get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




