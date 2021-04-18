---
description: Il metodo MakePalette crea una tavolozza logica dalla tabella dei colori in formato video.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Metodo CImagePalette. MakePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325064"
---
# <a name="cimagepalettemakepalette-method"></a>CImagePalette. MakePalette, metodo

Il `MakePalette` metodo crea una tavolozza logica dalla tabella dei colori in un formato video.

## <a name="syntax"></a>Sintassi


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) contenente la tabella dei colori.

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **ENUMDISPLAYDEVICES** GDI. Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se ha esito positivo, restituisce un handle per la tavolozza. In caso contrario, restituisce **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




