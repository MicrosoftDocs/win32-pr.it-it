---
description: Il metodo setavolozza installa una tavolozza per la finestra. Questo metodo non presenta parametri.
ms.assetid: 86eb34c6-85ff-4a40-8085-ea55dbc2727e
title: Metodo CBaseWindow. setavolozze (Winutil. h)-nessun parametro
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
ms.openlocfilehash: 1203b6aeedd39eb82d7188c4e5d5503b01d167fe
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104235234"
---
# <a name="cbasewindowsetpalette-method-winutilh---no-parameters"></a>Metodo CBaseWindow. setavolozze (Winutil. h)-nessun parametro

Il `SetPalette` metodo installa una tavolozza per la finestra.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPalette();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Una chiamata interna a **GDIFlush** ha restituito un errore.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Viene selezionata la tavolozza fornita dalla variabile membro [**CBaseWindow:: m \_ hPalette**](cbasewindow-m-hpalette.md) . Il chiamante deve garantire la validità di **m \_ hPalette**.

Se il valore della variabile membro [**\_ BNoRealize di CBaseWindow:: m**](cbasewindow-m-bnorealize.md) è **false** (impostazione predefinita), questo metodo seleziona la tavolozza e la realizza. In caso contrario, seleziona la tavolozza, ma non la realizza. L'oggetto non elimina le tavolozze precedenti utilizzate. Il chiamante è responsabile dell'eliminazione delle tavolozze.

Qualsiasi thread può chiamare in modo sicuro questo metodo, non solo il thread proprietario della finestra. La finestra Invia un messaggio privato a se stesso, che attiva una chiamata al metodo [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|-|-|
| Intestazione | WinUtil. h (include Streams. h) |
| Libreria| Strmbase. lib (compilazioni finali); Strmbasd. lib (build di debug) |

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




