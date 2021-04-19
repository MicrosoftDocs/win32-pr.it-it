---
description: La funzione ConvertVideoInfoToVideoInfo2 converte un tipo di supporto che usa VIDEOINFOHEADER in uno che usa VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: Funzione ConvertVideoInfoToVideoInfo2 (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324003"
---
# <a name="convertvideoinfotovideoinfo2-function"></a>ConvertVideoInfoToVideoInfo2 (funzione)

La `ConvertVideoInfoToVideoInfo2` funzione converte un tipo di supporto che usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) in uno che usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore alla struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) da convertire. Il formato del tipo di formato della struttura deve essere \_ videoinfo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce S \_ OK o e \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Questa funzione alloca una nuova struttura **VIDEOINFOHEADER2** , ne copia i membri della struttura **VIDEOINFOHEADER** e sostituisce la struttura precedente con la nuova struttura nel blocco di formato del tipo di supporto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni video e immagine](video-and-image-functions.md)
</dt> </dl>

 

 




