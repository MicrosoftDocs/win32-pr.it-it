---
description: Il metodo CheckPaletteHeader convalida le voci della tavolozza in una struttura VIDEOINFO.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Metodo CImageDisplay. CheckPaletteHeader (Winutil. h)
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
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331643"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>CImageDisplay. CheckPaletteHeader, metodo

Il `CheckPaletteHeader` metodo convalida le voci della tavolozza in una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

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

Puntatore a una struttura **VIDEOINFO** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se le voci della tavolozza sono valide o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se il formato dell'immagine non è pallettizzati, il metodo verifica che **biClrUsed** sia uguale a zero. In caso contrario, il metodo verifica che il flag di **bicompressione** sia bi \_ RGB; **biClrImportant** non è maggiore di **biClrUsed**; il numero di voci della tavolozza non supera il valore massimo, in base alla profondità del colore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImageDisplay**](cimagedisplay.md)
</dt> </dl>

 

 




