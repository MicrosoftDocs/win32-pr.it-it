---
description: 'Costruttore CMediaSample.CMediaSample : metodo del costruttore.'
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Costruttore CMediaSample.CMediaSample (Amfilter.h)
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
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095439"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="9bcf1-103">Costruttore CMediaSample.CMediaSample</span><span class="sxs-lookup"><span data-stu-id="9bcf1-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="9bcf1-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="9bcf1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bcf1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bcf1-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="9bcf1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bcf1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bcf1-107">*Pname*</span><span class="sxs-lookup"><span data-stu-id="9bcf1-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcf1-108">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="9bcf1-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="9bcf1-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="9bcf1-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcf1-110">Puntatore [**all'oggetto CBaseAllocator**](cbaseallocator.md) che ha creato questo esempio.</span><span class="sxs-lookup"><span data-stu-id="9bcf1-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="9bcf1-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="9bcf1-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcf1-112">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="9bcf1-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="9bcf1-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="9bcf1-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcf1-114">Puntatore a un buffer di memoria allocato dal chiamante, di lunghezza *.*</span><span class="sxs-lookup"><span data-stu-id="9bcf1-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="9bcf1-115">*length*</span><span class="sxs-lookup"><span data-stu-id="9bcf1-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="9bcf1-116">Lunghezza del buffer di memoria.</span><span class="sxs-lookup"><span data-stu-id="9bcf1-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9bcf1-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="9bcf1-117">Remarks</span></span>

<span data-ttu-id="9bcf1-118">La classe base non modifica il **valore HRESULT** passato nel *parametro phr.*</span><span class="sxs-lookup"><span data-stu-id="9bcf1-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bcf1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bcf1-119">Requirements</span></span>



| <span data-ttu-id="9bcf1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bcf1-120">Requirement</span></span> | <span data-ttu-id="9bcf1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="9bcf1-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bcf1-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9bcf1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9bcf1-123"><dt>Amfilter.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bcf1-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9bcf1-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="9bcf1-124">Library</span></span><br/> | <dl> <span data-ttu-id="9bcf1-125"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9bcf1-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bcf1-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9bcf1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bcf1-127">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="9bcf1-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




