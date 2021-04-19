---
description: Il metodo OnPaletteChange gestisce i messaggi di modifica della tavolozza.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Metodo CBaseWindow. OnPaletteChange (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.OnPaletteChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9abcb2d9f5cdc875f70f5c1db1fd2f625ce911f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325764"
---
# <a name="cbasewindowonpalettechange-method"></a>CBaseWindow. OnPaletteChange, metodo

Il `OnPaletteChange` metodo gestisce i messaggi di modifica della tavolozza.

## <a name="syntax"></a>Sintassi


```C++
virtual LRESULT OnPaletteChange(
   HWND hwnd,
   UINT Message
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*Messaggio* 
</dt> <dd>

Identificatore del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 se il messaggio è stato elaborato oppure 1 se il messaggio non è stato elaborato.

## <a name="remarks"></a>Commenti

Questo metodo gestisce \_ i messaggi WM PALETTECHANGED e WM \_ QUERYNEWPALETTE. Chiama il metodo [**CBaseWindow::D orealisepalette**](cbasewindow-dorealisepalette.md) per realizzare la nuova tavolozza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




