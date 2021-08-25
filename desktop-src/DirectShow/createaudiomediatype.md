---
description: La funzione CreateAudioMediaType inizializza un tipo di supporto da una struttura WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Funzione CreateAudioMediaType (Mtype.h)
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
ms.openlocfilehash: 2eb9dc01a398a498252cca2f1f3af012608f8e0ca80c62800c56e4026c0b0a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908821"
---
# <a name="createaudiomediatype-function"></a>Funzione CreateAudioMediaType

La **funzione CreateAudioMediaType** inizializza un tipo di supporto da una [**struttura WAVEFORMATEX.**](/previous-versions/dd757713(v=vs.85))

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

*Pmt* 
</dt> <dd>

Puntatore alla [**struttura AM \_ MEDIA \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) da inizializzare.

</dd> <dt>

*bSetFormat* 
</dt> <dd>

Flag che indica se inizializzare il blocco di formato. Specificare **TRUE per** inizializzarlo oppure FALSE in **caso** contrario.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce E \_ OUTOFMEMORY se non è stato possibile allocare memoria per i dati di formato. S \_ OK in caso contrario.

## <a name="remarks"></a>Commenti

Se il *parametro bSetFormat* è **TRUE,** il metodo alloca la memoria per il blocco di formato. Se il *parametro pmt* contiene già un blocco di formato allocato, si verificherà una perdita di memoria. Per evitare una perdita di memoria, chiamare [**FreeMediaType**](freemediatype.md) prima di chiamare questa funzione. Dopo la fine del metodo, chiamare **di nuovo FreeMediaType** per liberare il blocco di formato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Funzioni per i tipi di supporti**](media-type-functions.md)
</dt> </dl>

 

