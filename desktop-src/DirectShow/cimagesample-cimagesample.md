---
description: Costruttore CImageSample.CImageSample - Metodo costruttore.
ms.assetid: d7550c38-d728-41b2-80a6-20728abf6012
title: Costruttore CImageSample.CImageSample (Winutil.h)
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
ms.openlocfilehash: ecab52e347e03b698adccb79b77da879d26612b4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095609"
---
# <a name="cimagesamplecimagesample-constructor"></a><span data-ttu-id="3e57c-103">Costruttore CImageSample.CImageSample</span><span class="sxs-lookup"><span data-stu-id="3e57c-103">CImageSample.CImageSample constructor</span></span>

<span data-ttu-id="3e57c-104">Metodo del costruttore.</span><span class="sxs-lookup"><span data-stu-id="3e57c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e57c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e57c-105">Syntax</span></span>


```C++
CImageSample(
   CBaseAllocator *pAllocator,
   TCHAR          *pName,
   HRESULT        *phr,
   LPBYTE         pBuffer,
   LONG           length
);
```



## <a name="parameters"></a><span data-ttu-id="3e57c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e57c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e57c-107">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="3e57c-107">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="3e57c-108">Puntatore all'allocatore che ha creato questo esempio.</span><span class="sxs-lookup"><span data-stu-id="3e57c-108">Pointer to the allocator that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="3e57c-109">*Pname*</span><span class="sxs-lookup"><span data-stu-id="3e57c-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3e57c-110">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="3e57c-110">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3e57c-111">*Phr*</span><span class="sxs-lookup"><span data-stu-id="3e57c-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3e57c-112">Ignorato.</span><span class="sxs-lookup"><span data-stu-id="3e57c-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="3e57c-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="3e57c-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="3e57c-114">Puntatore a un buffer di memoria allocato dal chiamante di lunghezza *.*</span><span class="sxs-lookup"><span data-stu-id="3e57c-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span> <span data-ttu-id="3e57c-115">Il buffer deve contenere una bitmap GDI indipendente dal dispositivo (DIB).</span><span class="sxs-lookup"><span data-stu-id="3e57c-115">The buffer should contain a GDI device-independent bitmap (DIB).</span></span>

</dd> <dt>

<span data-ttu-id="3e57c-116">*length*</span><span class="sxs-lookup"><span data-stu-id="3e57c-116">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="3e57c-117">Lunghezza del buffer.</span><span class="sxs-lookup"><span data-stu-id="3e57c-117">Length of the buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e57c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e57c-118">Remarks</span></span>

<span data-ttu-id="3e57c-119">La [**classe CImageAllocator**](cimageallocator.md) crea un DIB usando un oggetto di mapping dei file supportato dal file di paging del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="3e57c-119">The [**CImageAllocator**](cimageallocator.md) class creates a DIB using a file-mapping object that is backed by the operating-system paging file.</span></span> <span data-ttu-id="3e57c-120">L'handle per l'oggetto di mapping dei file viene archiviato nel **membro hMapping** della **struttura \_ DibData m.**</span><span class="sxs-lookup"><span data-stu-id="3e57c-120">The handle to the file-mapping object is stored in the **hMapping** member of the **m\_DibData** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e57c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e57c-121">Requirements</span></span>



| <span data-ttu-id="3e57c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e57c-122">Requirement</span></span> | <span data-ttu-id="3e57c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3e57c-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e57c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e57c-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3e57c-125"><dt>Winutil.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e57c-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e57c-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="3e57c-126">Library</span></span><br/> | <dl> <span data-ttu-id="3e57c-127"><dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3e57c-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e57c-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e57c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e57c-129">**Classe CImageSample**</span><span class="sxs-lookup"><span data-stu-id="3e57c-129">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




