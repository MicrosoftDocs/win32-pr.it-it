---
description: Il metodo DoRealisePalette consente di realizzare il riquadro corrente della finestra.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Metodo CBaseWindow.DoRealisePalette (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ce593939ec9f8aa3f2675c95e7a70363465aabb6f501fde79de839c533a1d249
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757481"
---
# <a name="cbasewindowdorealisepalette-method"></a>Metodo CBaseWindow.DoRealisePalette

Il `DoRealisePalette` metodo realizza il riquadro corrente della finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bForceBackground* 
</dt> <dd>

Valore booleano che specifica se la tavolozza deve essere impostata come tavolozza di sfondo. Per altre informazioni, vedere **SelectPalette** in Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei **valori HRESULT** illustrati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Una chiamata interna a **GdiFlush ha** restituito un errore.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Operazione completata.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Il [**metodo CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) chiama questo metodo. Per impostare un nuovo riquadro, chiamare il [**metodo CBaseWindow::SetPalette.**](cbasewindow-setpalette.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




