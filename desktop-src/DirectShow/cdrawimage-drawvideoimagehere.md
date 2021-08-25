---
description: Il metodo DrawVideoImageHere disegna un'immagine da un campione multimediale a un contesto di dispositivo specificato.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Metodo CDrawImage.DrawVideoImageHere (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8137c4e18708ce6a0402d1d34caf9560054f267d8de0280a6efb5c3dd36e6517
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909811"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>Metodo CDrawImage.DrawVideoImageHere

Il `DrawVideoImageHere` metodo disegna un'immagine da un campione multimediale a un contesto di dispositivo specificato.

## <a name="syntax"></a>Sintassi


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hdc* 
</dt> <dd>

Handle a un contesto di dispositivo, in cui verrà eseguito il disegno.

</dd> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore [**all'interfaccia IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.

</dd> <dt>

*lprcSrc* 
</dt> <dd>

Puntatore a un rettangolo di origine da utilizzare per il disegno. Se **NULL,** viene usato il rettangolo in [**CDrawImage::m \_ SourceRect.**](cdrawimage-m-sourcerect.md)

</dd> <dt>

*lprcDst* 
</dt> <dd>

Puntatore a un rettangolo di destinazione da utilizzare per il disegno. Se **NULL,** viene usato il rettangolo in [**CDrawImage::m \_ TargetRect.**](cdrawimage-m-targetrect.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (include Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




