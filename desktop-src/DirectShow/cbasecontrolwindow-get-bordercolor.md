---
description: Il metodo get \_ BorderColor recupera il colore del bordo corrente.
ms.assetid: 4b4cae1d-bef7-4f8d-8011-c220fcfb73eb
title: CBaseControlWindow.get_BorderColor metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BorderColor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a351e794765f3dddb5275d8a588ca54ade06bb789ed720bfb17997fc11e358f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660755"
---
# <a name="cbasecontrolwindowget_bordercolor-method"></a>Metodo CBaseControlWindow.get \_ BorderColor

Il `get_BorderColor` metodo recupera il colore del bordo corrente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_BorderColor(
   long *Color
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Colore* 
</dt> <dd>

Puntatore al colore del bordo corrente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Un'applicazione può impostare un rettangolo di destinazione in cui deve essere visualizzato il video. Questo rettangolo è relativo all'area client per la finestra. Se questa operazione viene eseguita (per impostazione predefinita viene sempre disegnata l'intera finestra), è presente un bordo che circonda il video. Questa proprietà influisce sul colore utilizzato dal bordo. Anche se il parametro viene specificato come **tipo LONG,** è in realtà un **valore COLORREF.**

Questa funzione membro deve essere chiamata da oggetti esterni tramite [**l'interfaccia IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) e pertanto blocca la sezione critica per la sincronizzazione con il filtro associato. Chiamare la [**funzione membro CBaseControlWindow::GetBorderColour**](cbasecontrolwindow-getbordercolour.md) per recuperare questa proprietà se non viene chiamata da un oggetto esterno.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




