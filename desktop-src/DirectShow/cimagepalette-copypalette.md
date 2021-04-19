---
description: Il metodo CopyPalette copia la tavolozza da qualsiasi struttura VIDEOINFO a qualsiasi struttura pallettizzati VIDEOINFO.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Metodo CImagePalette. CopyPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332272"
---
# <a name="cimagepalettecopypalette-method"></a>CImagePalette. CopyPalette, metodo

Il `CopyPalette` metodo copia la tavolozza da qualsiasi struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) a qualsiasi struttura **VIDEOINFO** di pallettizzati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSrc* 
</dt> <dd>

Puntatore al tipo di supporto di origine.

</dd> <dt>

*pDest* 
</dt> <dd>

Puntatore al tipo di supporto di destinazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce \_ OK se la tavolozza è stata copiata. Restituisce \_ false se il tipo di supporto di origine o di destinazione non dispone di una tavolozza.

## <a name="remarks"></a>Commenti

Il tipo di supporto *pDest* deve essere un formato pallettizzati con una profondità di colore pari o inferiore a 8 bit. Il tipo di supporto *pSrc* può essere qualsiasi tipo [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con una tavolozza, inclusi i formati YUV e true-color con le voci della tavolozza. Il metodo copia le voci della tavolozza da *pSrc* in una nuova tavolozza e connette la nuova tavolozza a *pDest*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




