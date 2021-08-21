---
description: Il metodo get \_ BackgroundPalette recupera il riquadro realizzato nel flag di sfondo.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: CBaseControlWindow.get_BackgroundPalette metodo (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63ea3fa8ecbc6e644ccc5f4b1fac7a2fcd9c18270474f45dc08faa164f76cbec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660776"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>Metodo CBaseControlWindow.get \_ BackgroundPalette

Il `get_BackgroundPalette` metodo recupera il riquadro realizzato nel flag di sfondo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_BackgroundPalette(
   long *pBackgroundPalette
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pBackgroundPalette* 
</dt> <dd>

Puntatore a un flag booleano di automazione (0 è disattivato, 1 è on).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il [**metodo IVideoWindow::get \_ BackgroundPalette.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) Se un video verrà riprodotto all'interno di un'altra applicazione o documento, l'applicazione potrebbe voler usare la propria tavolozza. Può chiedere al video di usare la tavolozza in primo piano corrente anziché la propria impostando questo flag su 1. Se questa proprietà è impostata su 0, la finestra installa e realizza il proprio riquadro preferito. Si noti che chiedere alla finestra di usare un riquadro diverso causerà gravi penalità per le prestazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




