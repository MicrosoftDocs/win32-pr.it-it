---
description: Il metodo put \_ AutoShow imposta il flag di stato AutoShow.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: CBaseControlWindow.put_AutoShow metodo (Ctlutil.h)
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
ms.openlocfilehash: a8e24686baa3cf1f2ad570394acd7a290ac374043b8564566dc1e89668d3f6fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017279"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>Metodo \_ AutoShow CBaseControlWindow.put

Il `put_AutoShow` metodo imposta il flag di stato AutoShow.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Autoshow* 
</dt> <dd>

Flag booleano di automazione (0 è disattivato, 1 è on).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa proprietà semplifica l'accesso alla visualizzazione della finestra per le applicazioni. Se è impostata su 1 (attivata), la finestra, in genere nascosta dopo la connessione del filtro, verrà visualizzata automaticamente quando il filtro viene sospeso o eseguito. La finestra non deve tuttavia essere nascosta quando il filtro si arresta. Se questa proprietà è impostata su 0 (disattivata), la finestra viene resa visibile solo quando l'applicazione chiama [**CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con i parametri appropriati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




