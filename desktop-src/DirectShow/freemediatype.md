---
description: La funzione FreeMediaType elimina il blocco di formato in una struttura AM \_ MEDIA \_ TYPE.
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Funzione FreeMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4806a87674bf83964ad5b285934effd74b789ecebe7f92f642188b156bf1f48c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000506"
---
# <a name="freemediatype-function"></a>Funzione FreeMediaType

La **funzione FreeMediaType** elimina il blocco di formato in una [**struttura AM MEDIA \_ \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

## <a name="syntax"></a>Sintassi


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*mt* \[ Ref\]
</dt> <dd>

Riferimento a una [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Il blocco di formato viene allocato nell'heap. Il **membro pbFormat** di [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) punta al blocco di formato. Usare questa funzione per liberare solo il blocco di formato. Per eliminare una struttura **AM \_ MEDIA TYPE \_ allocata,** [**chiamare DeleteMediaType**](deletemediatype.md).

Questa funzione è definita nella libreria DirectShow [classi base.](directshow-base-classes.md) Se si preferisce non collegarsi alla libreria di classi di base, è possibile usare il codice seguente:


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Mtype.h (includere Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeleteMediaType**](deletemediatype.md)
</dt> <dt>

[**Funzioni per i tipi di supporti**](media-type-functions.md)
</dt> </dl>

 

 




