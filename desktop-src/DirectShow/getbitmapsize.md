---
description: La funzione GetBitmapSize calcola il numero di byte richiesti da una bitmap indipendente dal dispositivo (DIB). Questa funzione chiama semplicemente la macro DIBSIZE.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Funzione GetBitmapSize (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d736e0fa0766f1776fc53c39237242017de988050a469f4f16102d124d6f5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000263"
---
# <a name="getbitmapsize-function"></a>Funzione GetBitmapSize

La `GetBitmapSize` funzione calcola il numero di byte richiesti da una bitmap indipendente dal dispositivo (DIB). Questa funzione chiama semplicemente la macro [**DIBSIZE.**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize)

## <a name="syntax"></a>Sintassi


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pHeader* 
</dt> <dd>

Puntatore a una [**struttura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le dimensioni in byte.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per video e immagini](video-and-image-functions.md)
</dt> </dl>

 

 




