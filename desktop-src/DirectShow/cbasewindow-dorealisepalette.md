---
description: Il metodo DoRealisePalette realizza la tavolozza corrente della finestra.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Metodo CBaseWindow. DoRealisePalette (Winutil. h)
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
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325331"
---
# <a name="cbasewindowdorealisepalette-method"></a>CBaseWindow. DoRealisePalette, metodo

Il `DoRealisePalette` Metodo realizza la tavolozza corrente della finestra.

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

Valore booleano che specifica se la tavolozza è forzato a essere una tavolozza di sfondo. Per ulteriori informazioni, vedere **SelectPalette** in Platform SDK.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** indicati nella tabella seguente.



| Codice restituito                                                                             | Descrizione                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Una chiamata interna a **GDIFlush** ha restituito un errore.<br/> |
| <dl> <dt>**\_OK**</dt> </dl>    | Esito positivo.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Il metodo [**CBaseWindow:: OnPaletteChange**](cbasewindow-onpalettechange.md) chiama questo metodo. Per impostare una nuova tavolozza, chiamare il metodo [**CBaseWindow:: sepalette**](cbasewindow-setpalette.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




