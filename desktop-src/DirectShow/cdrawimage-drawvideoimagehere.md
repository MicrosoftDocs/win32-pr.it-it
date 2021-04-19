---
description: Il metodo DrawVideoImageHere disegna un'immagine da un campione multimediale a un contesto di dispositivo specificato.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Metodo CDrawImage. DrawVideoImageHere (Winutil. h)
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
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327211"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a>CDrawImage. DrawVideoImageHere, metodo

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

*HDC* 
</dt> <dd>

Handle per un contesto di dispositivo in cui si verificherà il disegno.

</dd> <dt>

*pMediaSample* 
</dt> <dd>

Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio che contiene l'immagine.

</dd> <dt>

*lprcSrc* 
</dt> <dd>

Puntatore a un rettangolo di origine da utilizzare per il disegno. Se **null**, viene utilizzato il rettangolo in [**CDrawImage:: m \_ sourceRect**](cdrawimage-m-sourcerect.md) .

</dd> <dt>

*lprcDst* 
</dt> <dd>

Puntatore a un rettangolo di destinazione da utilizzare per il disegno. Se **null**, viene utilizzato il rettangolo in [**CDrawImage:: m \_ targetRect**](cdrawimage-m-targetrect.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CDrawImage**](cdrawimage.md)
</dt> </dl>

 

 




