---
description: La funzione GetTrueColorType Recupera il nome leggibile di un sottotipo video.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Funzione GetTrueColorType (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328242"
---
# <a name="gettruecolortype-function"></a>GetTrueColorType (funzione)

La funzione **GetTrueColorType** Recupera il nome leggibile di un sottotipo video.

## <a name="syntax"></a>Sintassi


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pHeader* 
</dt> <dd>

Puntatore a una struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) che definisce la bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE \_ RGB565.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil. h (include Streams. h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni video e immagine](video-and-image-functions.md)
</dt> </dl>

 

 




