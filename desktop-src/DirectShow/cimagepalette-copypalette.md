---
description: Il metodo CopyPalette copia la tavolozza da qualsiasi struttura VIDEOINFO a qualsiasi struttura VIDEOINFO palettizzata.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Metodo CImagePalette.CopyPalette (Winutil.h)
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
ms.openlocfilehash: 5c6f645d134ccf5fa786ff59cf0bc6cd37211af0cb2571bbc9955e5bb6367a97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055451"
---
# <a name="cimagepalettecopypalette-method"></a>Metodo CImagePalette.CopyPalette

Il `CopyPalette` metodo copia la tavolozza da qualsiasi struttura [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) a qualsiasi struttura **VIDEOINFO** palettizzata.

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

Restituisce S \_ OK se il riquadro è stato copiato. Restituisce S \_ FALSE se il tipo di supporto di origine o di destinazione non dispone di un riquadro.

## <a name="remarks"></a>Commenti

Il *tipo di supporto pDest* deve essere un formato palettizzato con una profondità di colore di 8 bit o inferiore. Il tipo di supporto *pSrc* può essere qualsiasi [**tipo VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con una tavolozza, inclusi i formati YUV e true-color con voci della tavolozza. Il metodo copia le voci del riquadro da *pSrc* in un nuovo riquadro e associa il nuovo riquadro a *pDest*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CImagePalette**](cimagepalette.md)
</dt> </dl>

 

 




