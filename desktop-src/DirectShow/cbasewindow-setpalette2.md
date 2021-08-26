---
description: Il metodo SetPalette installa un riquadro per la finestra. Questo metodo non presenta parametri.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Metodo CBaseWindow.SetPalette (Winutil.h) - Nessun parametro
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
ms.openlocfilehash: f15df65f6e427e467c14654a0e2745b84d774a5226b9a526193fc546261c5a0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052151"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>Metodo CBaseWindow.SetPalette (Winutil.h) - Nessun parametro

Il `SetPalette` metodo installa un riquadro per la finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Una chiamata interna a **GdiFlush ha** restituito un errore.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                            |



 

## <a name="remarks"></a>Commenti

La tavolozza specificata dalla variabile membro [**CBaseWindow::m \_ hPalette**](cbasewindow-m-hpalette.md) è selezionata. Il chiamante deve garantire la validità di **m \_ hPalette**.

Se il valore della variabile membro [**CBaseWindow::m \_ bNoRealize**](cbasewindow-m-bnorealize.md) è **FALSE** (impostazione predefinita), questo metodo seleziona il riquadro e lo realizza. In caso contrario, seleziona il riquadro, ma non se ne rende conto. L'oggetto non elimina alcun riquadro precedente in uso. Il chiamante è responsabile dell'eliminazione dei tavolozze.

Qualsiasi thread può chiamare in modo sicuro questo metodo, non solo il thread proprietario della finestra. La finestra invia un messaggio privato a se stesso, che attiva una chiamata al metodo [**CBaseWindow::OnPaletteChange.**](cbasewindow-onpalettechange.md)

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | Winutil.h (include Flussi.h) |
| Libreria| Strmbase.lib (build di vendita al dettaglio); Strmbasd.lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




