---
description: Il metodo setpoint imposta il puntatore sul buffer di memoria.
ms.assetid: 60627600-c982-462e-b540-327a58e57615
title: Metodo CMediaSample. sepointer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetPointer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67d9fc5d260cc627919a458593328c36f0de9a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325310"
---
# <a name="cmediasamplesetpointer-method"></a><span data-ttu-id="045ed-103">CMediaSample. setpoint, metodo</span><span class="sxs-lookup"><span data-stu-id="045ed-103">CMediaSample.SetPointer method</span></span>

<span data-ttu-id="045ed-104">Il `SetPointer` metodo imposta il puntatore sul buffer di memoria.</span><span class="sxs-lookup"><span data-stu-id="045ed-104">The `SetPointer` method sets the pointer to the memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="045ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="045ed-105">Syntax</span></span>


```C++
HRESULT SetPointer(
   BYTE *ptr,
   LONG cBytes
);
```



## <a name="parameters"></a><span data-ttu-id="045ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="045ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="045ed-107">*ptr*</span><span class="sxs-lookup"><span data-stu-id="045ed-107">*ptr*</span></span> 
</dt> <dd>

<span data-ttu-id="045ed-108">Puntatore a un buffer di memoria allocato dal chiamante, di dimensioni *cBytes*.</span><span class="sxs-lookup"><span data-stu-id="045ed-108">Pointer to a memory buffer allocated by the caller, of size *cBytes*.</span></span>

</dd> <dt>

<span data-ttu-id="045ed-109">*cBytes*</span><span class="sxs-lookup"><span data-stu-id="045ed-109">*cBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="045ed-110">Lunghezza del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="045ed-110">Length of the buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="045ed-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="045ed-111">Return value</span></span>

<span data-ttu-id="045ed-112">Restituisce \_ OK.</span><span class="sxs-lookup"><span data-stu-id="045ed-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="045ed-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="045ed-113">Remarks</span></span>

<span data-ttu-id="045ed-114">Questo metodo consente all'allocatore di impostare un nuovo puntatore per l'esempio.</span><span class="sxs-lookup"><span data-stu-id="045ed-114">This method enables the allocator to set a new pointer for the sample.</span></span>

<span data-ttu-id="045ed-115">Questo metodo non è disponibile tramite l'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) .</span><span class="sxs-lookup"><span data-stu-id="045ed-115">This method is not available through the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="045ed-116">L'oggetto che crea l'esempio può accedere a questo metodo (tramite **CMediaSample**), ma gli altri oggetti non possono.</span><span class="sxs-lookup"><span data-stu-id="045ed-116">The object that creates the sample can access this method (through **CMediaSample**), but other objects cannot.</span></span>

## <a name="requirements"></a><span data-ttu-id="045ed-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="045ed-117">Requirements</span></span>



| <span data-ttu-id="045ed-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="045ed-118">Requirement</span></span> | <span data-ttu-id="045ed-119">Valore</span><span class="sxs-lookup"><span data-stu-id="045ed-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="045ed-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="045ed-120">Header</span></span><br/>  | <dl> <span data-ttu-id="045ed-121"><dt>Amfilter. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="045ed-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="045ed-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="045ed-122">Library</span></span><br/> | <dl> <span data-ttu-id="045ed-123"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="045ed-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="045ed-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="045ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="045ed-125">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="045ed-125">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




