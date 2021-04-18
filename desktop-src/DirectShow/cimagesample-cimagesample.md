---
description: Metodo del costruttore.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Costruttore CImageSample. CImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.CImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 805be59cfc899b6461fa8c761eebb5821118640f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325058"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="b12fb-103">Costruttore CImageSample. CImageSample</span><span class="sxs-lookup"><span data-stu-id="b12fb-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="b12fb-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="b12fb-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b12fb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b12fb-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="b12fb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b12fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b12fb-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="b12fb-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="b12fb-108">Puntatore all'allocatore che ha creato l'esempio.</span><span class="sxs-lookup"><span data-stu-id="b12fb-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="b12fb-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="b12fb-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b12fb-110">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="b12fb-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b12fb-111">*PHR*</span><span class="sxs-lookup"><span data-stu-id="b12fb-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b12fb-112">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="b12fb-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="b12fb-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="b12fb-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="b12fb-114">Puntatore a un buffer di memoria allocato dal chiamante, della *lunghezza* della dimensione.</span><span class="sxs-lookup"><span data-stu-id="b12fb-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="b12fb-115">Il buffer deve contenere una bitmap indipendente dal dispositivo (DIB) GDI.</span><span class="sxs-lookup"><span data-stu-id="b12fb-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="b12fb-116">*length*</span><span class="sxs-lookup"><span data-stu-id="b12fb-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="b12fb-117">Lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="b12fb-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b12fb-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="b12fb-118">Remarks</span></span>

<span data-ttu-id="b12fb-119">La classe [**CImageAllocator**](cimageallocator.md) crea una DIB usando un oggetto di mapping dei file supportato dal file di paging del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="b12fb-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="b12fb-120">L'handle per l'oggetto di mapping dei file viene archiviato nel membro **hMapping** della struttura **m \_ DibData** .</span><span class="sxs-lookup"><span data-stu-id="b12fb-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b12fb-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b12fb-121">Requirements</span></span>



| <span data-ttu-id="b12fb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b12fb-122">Requirement</span></span> | <span data-ttu-id="b12fb-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b12fb-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b12fb-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b12fb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b12fb-125"><dt>WinUtil. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b12fb-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b12fb-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b12fb-126">Library</span></span><br/> | <dl> <span data-ttu-id="b12fb-127"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b12fb-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b12fb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b12fb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b12fb-129">**Classe CImageSample**</span><span class="sxs-lookup"><span data-stu-id="b12fb-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




