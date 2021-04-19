---
description: Il metodo PaintWindow fa sì che la finestra venga ridisegnata.
ms.assetid: dce3d782-00e5-4176-9365-378d59d48ebc
title: Metodo CBaseWindow. PaintWindow (Winutil. h)
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
ms.openlocfilehash: 3b0932422f85cb31d587485976dfacbaa51e2bf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332589"
---
# <a name="cbasewindowpaintwindow-method"></a>CBaseWindow. PaintWindow, metodo

Il `PaintWindow` metodo fa sì che la finestra venga ridisegnata.

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

Valore booleano che specifica se lo sfondo è stato cancellato. Se il valore è **true**, lo sfondo viene cancellato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo genera un \_ messaggio di disegno WM invalidando l'intera area client della finestra.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




