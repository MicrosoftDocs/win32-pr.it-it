---
description: La funzione GetTrueColorType recupera il nome leggibile dall'utente di un sottotipo video.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Funzione GetTrueColorType (Wxutil.h)
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
ms.openlocfilehash: 3fb25d4539d4b929362241ffacbfafd97b08844508ec2c1f38c619fe40901475
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119564711"
---
# <a name="gettruecolortype-function"></a>Funzione GetTrueColorType

La **funzione GetTrueColorType** recupera il nome leggibile dall'utente di un sottotipo video.

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

Puntatore a una [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) che definisce la bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE \_ RGB565.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per video e immagini](video-and-image-functions.md)
</dt> </dl>

 

 




