---
description: Il metodo SetPalette installa una tavolozza per la finestra.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Metodo CBaseWindow.SetPalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.SetPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c04d4e24c621dd704b8aeba91646016e334a6f6bface4769578a710322a7cff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074555"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a>Metodo CBaseWindow.SetPalette (Winutil.h)

Il `SetPalette` metodo installa una tavolozza per la finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT SetPalette(
   HPALETTE hPalette
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hPalette* 
</dt> <dd>

Handle per la nuova tavolozza. Non può essere **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Una chiamata interna a **GdiFlush ha** restituito un errore.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Se il valore della variabile membro [**CBaseWindow::m \_ bNoRealize**](cbasewindow-m-bnorealize.md) è **FALSE** (impostazione predefinita), questo metodo seleziona la tavolozza e la rende disponibile. In caso contrario, seleziona la tavolozza, ma non se ne rende conto. L'oggetto non elimina la tavolozza precedente in uso. Il chiamante è responsabile dell'eliminazione delle tavolozze.

Qualsiasi thread può chiamare in modo sicuro questo metodo, non solo il thread proprietario della finestra. La finestra invia un messaggio privato a se stessa, che attiva una chiamata al [**metodo CBaseWindow::OnPaletteChange.**](cbasewindow-onpalettechange.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




