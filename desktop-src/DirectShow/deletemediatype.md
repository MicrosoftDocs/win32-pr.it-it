---
description: La funzione DeleteMediaType elimina una struttura AM \_ MEDIA \_ TYPE allocata, incluso il blocco di formato.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Funzione DeleteMediaType (Mtype.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6035b65d6bf292f6ca35c4323ac5ad90c747b0cfd4bfa756b1f054d7b693d998
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998391"
---
# <a name="deletemediatype-function"></a>Funzione DeleteMediaType

La **funzione DeleteMediaType** elimina una struttura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) allocata, incluso il blocco di formato.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pmt* 
</dt> <dd>

Puntatore a una [**struttura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Usare questa funzione per rilasciare qualsiasi struttura di tipo di supporto allocata usando [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) [**o CreateMediaType**](createmediatype.md).

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


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
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

[**FreeMediaType**](freemediatype.md)
</dt> <dt>

[**Funzioni del tipo di supporto**](media-type-functions.md)
</dt> </dl>

 

