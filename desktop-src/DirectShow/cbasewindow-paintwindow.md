---
description: Il metodo PaintWindow fa sì che la finestra sia ridisegnata.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Metodo CBaseWindow.PaintWindow (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.PaintWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cc998f270947890327fb3cbacce4a29183604047824b05b8a66538c163bdc08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635121"
---
# <a name="cbasewindowpaintwindow-method"></a>Metodo CBaseWindow.PaintWindow

Il `PaintWindow` metodo fa sì che la finestra sia ridisegnata.

## <a name="syntax"></a>Sintassi


```C++
void PaintWindow(
   BOOL bErase
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bErase* 
</dt> <dd>

Valore booleano che specifica se lo sfondo viene cancellato. Se il valore è **TRUE,** lo sfondo viene cancellato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo genera un messaggio WM \_ PAINT invalidando l'intera area client della finestra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




