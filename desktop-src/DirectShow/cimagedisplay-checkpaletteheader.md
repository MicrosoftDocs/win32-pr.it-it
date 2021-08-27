---
description: Il metodo CheckPaletteHeader convalida le voci della tavolozza in una struttura VIDEOINFO.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Metodo CImageDisplay.CheckPaletteHeader (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6378a93ffced86546b8e95071e7f9bdc1398cdd1831aa18d41d62c6ea97caff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087291"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>Metodo CImageDisplay.CheckPaletteHeader

Il `CheckPaletteHeader` metodo convalida le voci del riquadro in una struttura [**VIDEOINFO.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)

## <a name="syntax"></a>Sintassi


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pInput* 
</dt> <dd>

Puntatore a una **struttura VIDEOINFO.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE se** le voci del riquadro sono valide oppure FALSE in caso **contrario.**

## <a name="remarks"></a>Commenti

Se il formato dell'immagine non è chiaro, il metodo verifica che **biClrUsed** sia uguale a zero. In caso contrario, il metodo verifica che il flag **biCompression** sia BI \_ RGB. **biClrImportant** non è maggiore di **biClrUsed;** e il numero di voci della tavolozza non supera il valore massimo, data la profondità del colore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




