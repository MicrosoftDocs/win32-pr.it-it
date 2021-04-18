---
description: Il \_ metodo Put Autoshow imposta il flag di stato di visualizzazione.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Metodo CBaseControlWindow.put_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327225"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>CBaseControlWindow. put \_ AutoShow (metodo)

Il `put_AutoShow` metodo imposta il flag di stato di visualizzazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AutoShow* 
</dt> <dd>

Flag booleano di automazione (0 è disattivato, 1 è on).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa proprietà semplifica l'accesso alla visualizzazione delle finestre per le applicazioni. Se questa impostazione è impostata su 1 (on), la finestra, che in genere è nascosta dopo la connessione del filtro, verrà visualizzata automaticamente quando il filtro viene sospeso o eseguito. Tuttavia, la finestra non deve essere nascosta quando il filtro si arresta. Se è impostato su 0 (disattivato), la finestra viene resa visibile solo quando l'applicazione chiama [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con i parametri appropriati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




