---
description: La funzione CreateAudioMediaType Inizializza un tipo di supporto da una struttura WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Funzione CreateAudioMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331320"
---
# <a name="createaudiomediatype-function"></a>CreateAudioMediaType (funzione)

La funzione **CreateAudioMediaType** Inizializza un tipo di supporto da una struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pwfx* 
</dt> <dd>

Puntatore alla struttura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) fornita.

</dd> <dt>

*PMT* 
</dt> <dd>

Puntatore alla struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) da inizializzare.

</dd> <dt>

*bSetFormat* 
</dt> <dd>

Flag che indica se inizializzare il blocco di formato. Specificare **true** per inizializzarlo o **false** in caso contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ OutOfMemory se non è stato possibile allocare memoria per i dati del formato. S \_ OK in caso contrario.

## <a name="remarks"></a>Commenti

Se il parametro *bSetFormat* è **true**, il metodo alloca la memoria per il blocco di formato. Se il parametro *PMT* contiene già un blocco di formato allocato, si verificherà una perdita di memoria. Per evitare una perdita di memoria, chiamare [**FreeMediaType**](freemediatype.md) prima di chiamare questa funzione. Quando il metodo restituisce un risultato, chiamare di nuovo **FreeMediaType** per liberare il blocco di formato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni di tipo multimediale**](media-type-functions.md)
</dt> </dl>

 

