---
description: Il metodo setavolozza installa una tavolozza per la finestra.
ms.assetid: 64fa0d3a-c2eb-4e58-8b8d-c8e5ec3bb479
title: Metodo CBaseWindow. setavolozze (Winutil. h)
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
ms.openlocfilehash: f246fe8401e1f671f5935ff7d7454093ea1d3179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325757"
---
# <a name="cbasewindowsetpalette-method-winutilh"></a>Metodo CBaseWindow. setavolozze (Winutil. h)

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

Handle per la nuova tavolozza. Non può essere **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Una chiamata interna a **GDIFlush** ha restituito un errore.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Se il valore della variabile membro [**\_ BNoRealize di CBaseWindow:: m**](cbasewindow-m-bnorealize.md) è **false** (impostazione predefinita), questo metodo seleziona la tavolozza e la realizza. In caso contrario, seleziona la tavolozza, ma non la realizza. L'oggetto non elimina le tavolozze precedenti utilizzate. Il chiamante è responsabile dell'eliminazione delle tavolozze.

Qualsiasi thread può chiamare in modo sicuro questo metodo, non solo il thread proprietario della finestra. La finestra Invia un messaggio privato a se stesso, che attiva una chiamata al metodo [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




