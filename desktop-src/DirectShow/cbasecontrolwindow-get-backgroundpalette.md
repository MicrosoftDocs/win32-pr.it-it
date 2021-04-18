---
description: Il \_ metodo Get BackgroundPalette recupera la tavolozza realizzata nel flag di sfondo.
ms.assetid: cc649dbd-d049-4993-b187-4e297bef5152
title: Metodo CBaseControlWindow.get_BackgroundPalette (Ctlutil. h)
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
ms.openlocfilehash: dd06bcec9b3c435370ec3f12340c1c3aede3904c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325394"
---
# <a name="cbasecontrolwindowget_backgroundpalette-method"></a>Metodo CBaseControlWindow. Get \_ BackgroundPalette

Il `get_BackgroundPalette` metodo recupera la tavolozza realizzata nel flag di sfondo.

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

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Questa funzione membro implementa il metodo [**IVideoWindow:: Get \_ BackgroundPalette**](/windows/desktop/api/Control/nf-control-ivideowindow-get_backgroundpalette) . Se un video viene riprodotto all'interno di un'altra applicazione o documento, l'applicazione potrebbe voler usare la propria tavolozza. È possibile che il video usi la tavolozza di primo piano corrente anziché la propria impostando questo flag su 1. Se questa proprietà è impostata su 0, la finestra verrà installata e si renderà conto della tavolozza preferita. Si noti che la richiesta della finestra di utilizzare una tavolozza diversa provocherà gravi sanzioni in termini di prestazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




