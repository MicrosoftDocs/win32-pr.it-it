---
description: La funzione ContainsPalette determina se una struttura VIDEOINFOHEADER specificata contiene una tavolozza.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Funzione ContainsPalette (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329761"
---
# <a name="containspalette-function"></a>ContainsPalette (funzione)

La funzione **ContainsPalette** determina se una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) specificata contiene una tavolozza.

## <a name="syntax"></a>Sintassi


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pVideoInfo* 
</dt> <dd>

Puntatore a una struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se bitdepth è 8 o less (**bmiHeader. biBitCount**) o il numero di indici di colore è maggiore di zero (**bmiHeader. biClrUsed**). In caso contrario, restituisce **false** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni video e immagine](video-and-image-functions.md)
</dt> </dl>

 

 




