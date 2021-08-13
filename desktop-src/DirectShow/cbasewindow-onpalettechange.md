---
description: Il metodo OnPaletteChange gestisce i messaggi di modifica della tavolozza.
ms.assetid: 2abae4f1-fbd0-4a32-8772-012fa96b6d6c
title: Metodo CBaseWindow.OnPaletteChange (Winutil.h)
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
ms.openlocfilehash: c881c519706ca0288847a7dc603cf513a99cdd76e4c83f0e53bec16df840e509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657954"
---
# <a name="cbasewindowonpalettechange-method"></a>Metodo CBaseWindow.OnPaletteChange

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

*Hwnd* 
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

Questo metodo gestisce i messaggi WM \_ PALETTECHANGED e WM \_ QUERYNEWPALETTE. Chiama il metodo [**CBaseWindow::D oRealisePalette**](cbasewindow-dorealisepalette.md) per realizzare la nuova tavolozza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




