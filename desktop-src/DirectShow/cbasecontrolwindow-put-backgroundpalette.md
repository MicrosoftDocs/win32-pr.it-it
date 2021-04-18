---
description: Il \_ metodo Put BackgroundPalette imposta un flag per realizzare la tavolozza in background.
ms.assetid: db420e75-e300-41fa-bae4-fb267cc99c7c
title: Metodo CBaseControlWindow.put_BackgroundPalette (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_BackgroundPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 04aeb445be91426e7995ecd01c9326cda586a447
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328355"
---
# <a name="cbasecontrolwindowput_backgroundpalette-method"></a>CBaseControlWindow. put \_ BackgroundPalette (metodo)

Il `put_BackgroundPalette` metodo imposta un flag per realizzare la tavolozza in background.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_BackgroundPalette(
   long BackgroundPalette
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*BackgroundPalette* 
</dt> <dd>

Flag booleano di automazione (0 è disattivato, 1 è on).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Per riprodurre un video all'interno di un'altra applicazione o documento, l'applicazione potrebbe voler usare la propria tavolozza. È possibile che il video usi la tavolozza di primo piano corrente anziché la relativa tavolozza, impostando questo flag su 1. Se questa proprietà è impostata su 0, la finestra verrà installata e si renderà conto della tavolozza preferita. La richiesta di utilizzo di una tavolozza diversa provocherà gravi sanzioni in termini di prestazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




