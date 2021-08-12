---
description: Il metodo IsAutoShowEnabled recupera informazioni sulla visualizzazione automatica della finestra video quando il filtro di rendering viene sospeso o eseguito.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Metodo CBaseControlWindow.IsAutoShowEnabled (Ctlutil.h)
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
ms.openlocfilehash: 81f5190d3b0634c763703a3e13aa711f097641285f49c469dab6bad6ce0d9055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660230"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>Metodo CBaseControlWindow.IsAutoShowEnabled

Il metodo recupera informazioni sulla visualizzazione automatica della finestra video quando il filtro `IsAutoShowEnabled` di rendering viene sospeso o eseguito.

## <a name="syntax"></a>Sintassi


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE** se il **membro m \_ bAutoShow** è impostato su 1 o **FALSE** se è impostato su 0.

## <a name="remarks"></a>Commenti

Se il **membro m \_ bAutoShow** è impostato su 1 in una finestra video nascosta, la finestra diventa visibile quando il filtro viene sospeso o eseguito. Se questo membro è impostato su 0, la finestra verrà visualizzata solo se si usa la funzione membro [**CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con i parametri appropriati.

Questa funzione membro recupera l'impostazione del membro **m \_ bAutoShow** e ha lo stesso risultato dell'uso del metodo [**IVideoWindow::get \_ AutoShow.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




