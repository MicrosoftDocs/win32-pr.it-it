---
description: Metodo del costruttore.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Costruttore CMediaSample. CMediaSample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326408"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="46968-103">Costruttore CMediaSample. CMediaSample</span><span class="sxs-lookup"><span data-stu-id="46968-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="46968-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="46968-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="46968-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46968-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="46968-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="46968-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46968-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="46968-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="46968-108">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="46968-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="46968-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="46968-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="46968-110">Puntatore all'oggetto [**CBaseAllocator**](cbaseallocator.md) che ha creato l'esempio.</span><span class="sxs-lookup"><span data-stu-id="46968-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="46968-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="46968-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="46968-112">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="46968-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="46968-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="46968-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="46968-114">Puntatore a un buffer di memoria allocato dal chiamante, della *lunghezza* della dimensione.</span><span class="sxs-lookup"><span data-stu-id="46968-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="46968-115">*length*</span><span class="sxs-lookup"><span data-stu-id="46968-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="46968-116">Lunghezza del buffer di memoria.</span><span class="sxs-lookup"><span data-stu-id="46968-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="46968-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="46968-117">Remarks</span></span>

<span data-ttu-id="46968-118">La classe base non modifica il valore **HRESULT** passato nel parametro *PHR* .</span><span class="sxs-lookup"><span data-stu-id="46968-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="46968-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="46968-119">Requirements</span></span>



| <span data-ttu-id="46968-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="46968-120">Requirement</span></span> | <span data-ttu-id="46968-121">Valore</span><span class="sxs-lookup"><span data-stu-id="46968-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46968-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="46968-122">Header</span></span><br/>  | <dl> <span data-ttu-id="46968-123"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46968-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="46968-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="46968-124">Library</span></span><br/> | <dl> <span data-ttu-id="46968-125"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="46968-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46968-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46968-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46968-127">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="46968-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




