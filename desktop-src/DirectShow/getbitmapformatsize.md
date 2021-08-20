---
description: La funzione GetBitmapFormatSize calcola le dimensioni necessarie per una struttura VIDEOINFO che può contenere una struttura BITMAPINFOHEADER specificata.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: Funzione GetBitmapFormatSize (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1325073180634c21c29ff8ad09d255368c7d13e5e7d0a42f6fe5db4d6beba1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000293"
---
# <a name="getbitmapformatsize-function"></a>Funzione GetBitmapFormatSize

La `GetBitmapFormatSize` funzione calcola le dimensioni necessarie per una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) che può contenere una [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) specificata.

## <a name="syntax"></a>Sintassi


```C++
LONG GetBitmapFormatSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pHeader* 
</dt> <dd>

Puntatore a [**una struttura BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce le dimensioni, in byte.

## <a name="remarks"></a>Commenti

Una [**struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) può essere seguita da maschere di colore o voci della tavolozza, pertanto può essere difficile determinare il numero di byte necessari per costruire una struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) da una struttura **BITMAPINFOHEADER esistente.**

Per copiare [**una struttura BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) in [**una struttura VIDEOINFO,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) usare la macro [**HEADER,**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) che calcola l'offset corretto.

## <a name="examples"></a>Esempio


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Wxutil.h (includere Flussi.h)</dt> </dl>                                                                                    |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per video e immagini](video-and-image-functions.md)
</dt> </dl>

 

 




