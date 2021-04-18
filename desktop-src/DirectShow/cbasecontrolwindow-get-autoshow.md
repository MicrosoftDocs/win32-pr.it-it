---
description: Il \_ metodo Get Autoshow Recupera il flag di stato di Autoshow corrente.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Metodo CBaseControlWindow.get_AutoShow (Ctlutil. h)
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
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325388"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>CBaseControlWindow. Get \_ AutoShow (metodo)

Il `get_AutoShow` metodo recupera il flag di stato di Autoshow corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AutoShow* 
</dt> <dd>

Puntatore a un flag booleano di automazione (0 è disattivato, 1 è on).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IVideoWindow:: Get \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) . Questa proprietà semplifica l'accesso alla visualizzazione delle finestre per le applicazioni. Se questa impostazione è impostata su 1 (on), la finestra, che in genere viene nascosta dopo la connessione del filtro, verrà visualizzata automaticamente quando il filtro viene sospeso o eseguito. Tuttavia, la finestra non deve essere nascosta quando il filtro si arresta. Se questo parametro è impostato su 0 (disattivato), la finestra viene resa visibile solo quando l'applicazione chiama [**CBaseControlWindow::p UT \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con i parametri appropriati.

Questa funzione membro deve essere chiamata da oggetti esterni tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e pertanto blocca la sezione critica per la sincronizzazione con il filtro associato. Chiamare la funzione membro [**CBaseControlWindow:: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) per recuperare questa proprietà se non si chiama da un oggetto esterno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




