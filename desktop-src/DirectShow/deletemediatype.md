---
description: La funzione DeleteMediaType Elimina una \_ struttura del tipo di supporto am allocata \_ , incluso il blocco di formato.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Funzione DeleteMediaType (mtype. h)
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
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326390"
---
# <a name="deletemediatype-function"></a>DeleteMediaType (funzione)

La funzione **DeleteMediaType** Elimina una struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allocata, incluso il blocco di formato.

## <a name="syntax"></a>Sintassi


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PMT* 
</dt> <dd>

Puntatore a una struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questa funzione non restituisce un valore.

## <a name="remarks"></a>Commenti

Utilizzare questa funzione per rilasciare qualsiasi struttura del tipo di supporto allocata utilizzando [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) o [**CreateMediaType**](createmediatype.md).

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
| Intestazione<br/>  | <dl> <dt>Mtype. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**FreeMediaType**](freemediatype.md)
</dt> <dt>

[**Funzioni di tipo multimediale**](media-type-functions.md)
</dt> </dl>

 

