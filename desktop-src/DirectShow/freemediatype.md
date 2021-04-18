---
description: La funzione FreeMediaType Elimina il blocco di formato in una \_ struttura del tipo di supporto am \_ .
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Funzione FreeMediaType (mtype. h)
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
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331439"
---
# <a name="freemediatype-function"></a>FreeMediaType (funzione)

La funzione **FreeMediaType** Elimina il blocco di formato in una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

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

Riferimento a una struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Il blocco di formato viene allocato nell'heap. Il membro **pbFormat** del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) punta al blocco di formato. Usare questa funzione per liberare solo il blocco di formato. Per eliminare una struttura **del \_ \_ tipo di supporto am** allocata, chiamare [**DeleteMediaType**](deletemediatype.md).

Questa funzione è definita nella libreria di [classi base DirectShow](directshow-base-classes.md) . Se si preferisce non eseguire il collegamento alla libreria di classi di base, è possibile usare il codice seguente:


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
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DeleteMediaType**](deletemediatype.md)
</dt> <dt>

[**Funzioni di tipo multimediale**](media-type-functions.md)
</dt> </dl>

 

 




