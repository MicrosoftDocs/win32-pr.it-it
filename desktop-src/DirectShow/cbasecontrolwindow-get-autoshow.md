---
description: Il metodo get \_ AutoShow recupera il flag di stato AutoShow corrente.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: CBaseControlWindow.get_AutoShow metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7a5c16e0b460d07255cae113194f672ca3dace6f46827ac613c9559370284beb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158794"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>Metodo CBaseControlWindow.get \_ AutoShow

Il `get_AutoShow` metodo recupera il flag di stato AutoShow corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Autoshow* 
</dt> <dd>

Puntatore a un flag booleano di automazione (0 è disattivato, 1 è on).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IVideoWindow::get \_ AutoShow.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) Questa proprietà semplifica l'accesso alla visualizzazione della finestra per le applicazioni. Se è impostato su 1 (on), la finestra, in genere nascosta dopo la connessione del filtro, verrà visualizzata automaticamente quando il filtro viene sospeso o eseguito. Tuttavia, la finestra non deve essere nascosta quando il filtro si arresta. Se questo parametro è impostato su 0 (disattivato), la finestra viene resa visibile solo quando l'applicazione chiama [**CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con i parametri appropriati.

Questa funzione membro deve essere chiamata da oggetti esterni tramite [**l'interfaccia IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e pertanto blocca la sezione critica per la sincronizzazione con il filtro associato. Chiamare la funzione membro [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) per recuperare questa proprietà se non si chiama da un oggetto esterno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




