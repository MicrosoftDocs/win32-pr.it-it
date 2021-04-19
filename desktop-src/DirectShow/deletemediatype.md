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
# <a name="deletemediatype-function"></a><span data-ttu-id="00fee-103">DeleteMediaType (funzione)</span><span class="sxs-lookup"><span data-stu-id="00fee-103">DeleteMediaType function</span></span>

<span data-ttu-id="00fee-104">La funzione **DeleteMediaType** Elimina una struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) allocata, incluso il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="00fee-104">The **DeleteMediaType** function deletes an allocated [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="00fee-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00fee-105">Syntax</span></span>


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="00fee-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00fee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00fee-107">*PMT*</span><span class="sxs-lookup"><span data-stu-id="00fee-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="00fee-108">Puntatore a una struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="00fee-108">A pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00fee-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00fee-109">Return value</span></span>

<span data-ttu-id="00fee-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="00fee-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00fee-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="00fee-111">Remarks</span></span>

<span data-ttu-id="00fee-112">Utilizzare questa funzione per rilasciare qualsiasi struttura del tipo di supporto allocata utilizzando [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) o [**CreateMediaType**](createmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="00fee-112">Use this function to release any media type structure that was allocated using either [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) or [**CreateMediaType**](createmediatype.md).</span></span>

<span data-ttu-id="00fee-113">Questa funzione è definita nella libreria di [classi base DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="00fee-113">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="00fee-114">Se si preferisce non eseguire il collegamento alla libreria di classi di base, è possibile usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="00fee-114">If you prefer not to link to the base class library, you can use the following code:</span></span>


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





## <a name="requirements"></a><span data-ttu-id="00fee-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00fee-115">Requirements</span></span>



| <span data-ttu-id="00fee-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="00fee-116">Requirement</span></span> | <span data-ttu-id="00fee-117">Valore</span><span class="sxs-lookup"><span data-stu-id="00fee-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00fee-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="00fee-118">Header</span></span><br/>  | <dl> <span data-ttu-id="00fee-119"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00fee-119"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="00fee-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="00fee-120">Library</span></span><br/> | <dl> <span data-ttu-id="00fee-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="00fee-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00fee-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00fee-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00fee-123">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="00fee-123">**FreeMediaType**</span></span>](freemediatype.md)
</dt> <dt>

[<span data-ttu-id="00fee-124">**Funzioni di tipo multimediale**</span><span class="sxs-lookup"><span data-stu-id="00fee-124">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

