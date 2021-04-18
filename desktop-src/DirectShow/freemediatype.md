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
# <a name="freemediatype-function"></a><span data-ttu-id="d1b0e-103">FreeMediaType (funzione)</span><span class="sxs-lookup"><span data-stu-id="d1b0e-103">FreeMediaType function</span></span>

<span data-ttu-id="d1b0e-104">La funzione **FreeMediaType** Elimina il blocco di formato in una struttura del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="d1b0e-104">The **FreeMediaType** function deletes the format block in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b0e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d1b0e-105">Syntax</span></span>


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a><span data-ttu-id="d1b0e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d1b0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1b0e-107">*mt* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="d1b0e-107">*mt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d1b0e-108">Riferimento a una struttura [**del \_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="d1b0e-108">A reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1b0e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d1b0e-109">Return value</span></span>

<span data-ttu-id="d1b0e-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d1b0e-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1b0e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d1b0e-111">Remarks</span></span>

<span data-ttu-id="d1b0e-112">Il blocco di formato viene allocato nell'heap.</span><span class="sxs-lookup"><span data-stu-id="d1b0e-112">The format block is allocated on the heap.</span></span> <span data-ttu-id="d1b0e-113">Il membro **pbFormat** del [**\_ \_ tipo di supporto am**](/windows/win32/api/strmif/ns-strmif-am_media_type) punta al blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="d1b0e-113">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) points to the format block.</span></span> <span data-ttu-id="d1b0e-114">Usare questa funzione per liberare solo il blocco di formato.</span><span class="sxs-lookup"><span data-stu-id="d1b0e-114">Use this function to free just the format block.</span></span> <span data-ttu-id="d1b0e-115">Per eliminare una struttura **del \_ \_ tipo di supporto am** allocata, chiamare [**DeleteMediaType**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="d1b0e-115">To delete an allocated **AM\_MEDIA\_TYPE** structure, call [**DeleteMediaType**](deletemediatype.md).</span></span>

<span data-ttu-id="d1b0e-116">Questa funzione è definita nella libreria di [classi base DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="d1b0e-116">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="d1b0e-117">Se si preferisce non eseguire il collegamento alla libreria di classi di base, è possibile usare il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="d1b0e-117">If you prefer not to link to the base class library, you can use the following code:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d1b0e-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d1b0e-118">Requirements</span></span>



| <span data-ttu-id="d1b0e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1b0e-119">Requirement</span></span> | <span data-ttu-id="d1b0e-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d1b0e-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b0e-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d1b0e-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d1b0e-122"><dt>Mtype. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1b0e-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d1b0e-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="d1b0e-123">Library</span></span><br/> | <dl> <span data-ttu-id="d1b0e-124"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d1b0e-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b0e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d1b0e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b0e-126">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="d1b0e-126">**DeleteMediaType**</span></span>](deletemediatype.md)
</dt> <dt>

[<span data-ttu-id="d1b0e-127">**Funzioni di tipo multimediale**</span><span class="sxs-lookup"><span data-stu-id="d1b0e-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




