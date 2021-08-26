---
description: Il metodo MakePalette crea una tavolozza logica dalla tabella dei colori in un formato video.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Metodo CImagePalette.MakePalette (Winutil.h)
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
ms.openlocfilehash: f270797c224617c02b14752b15bbdb54b64a7457670e0b26bae54c39a93657eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055391"
---
# <a name="cimagepalettemakepalette-method"></a>Metodo CImagePalette.MakePalette

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

Puntatore a una [**struttura VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) che contiene la tabella dei colori.

</dd> <dt>

*szDevice* 
</dt> <dd>

Puntatore a una stringa che contiene il nome del dispositivo di visualizzazione, come restituito dalla funzione **GDI EnumDisplayDevices.** Per usare il dispositivo di visualizzazione principale, impostare questo parametro su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

In caso di esito positivo, restituisce un handle al riquadro. In caso contrario, restituisce **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




