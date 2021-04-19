---
description: Il metodo Copy copia un esempio di supporto.
ms.assetid: 3fbc6925-6e9c-4419-ab0d-0bbdbdf9bb8e
title: Metodo CTransInPlaceFilter. Copy (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Copy
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3063427611cd3a5aae74fecf6be273c07fdb917c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332977"
---
# <a name="ctransinplacefiltercopy-method"></a><span data-ttu-id="30778-103">Metodo CTransInPlaceFilter. Copy</span><span class="sxs-lookup"><span data-stu-id="30778-103">CTransInPlaceFilter.Copy method</span></span>

<span data-ttu-id="30778-104">Il `Copy` metodo copia un esempio di supporto.</span><span class="sxs-lookup"><span data-stu-id="30778-104">The `Copy` method copies a media sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="30778-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30778-105">Syntax</span></span>


```C++
IMediaSample* Copy(
   IMediaSample *pSource
);
```



## <a name="parameters"></a><span data-ttu-id="30778-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="30778-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30778-107">*pSource*</span><span class="sxs-lookup"><span data-stu-id="30778-107">*pSource*</span></span> 
</dt> <dd>

<span data-ttu-id="30778-108">Puntatore all'interfaccia [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) dell'esempio.</span><span class="sxs-lookup"><span data-stu-id="30778-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30778-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30778-109">Return value</span></span>

<span data-ttu-id="30778-110">Restituisce un puntatore all'interfaccia **IMediaSample** del nuovo campione.</span><span class="sxs-lookup"><span data-stu-id="30778-110">Returns a pointer to the **IMediaSample** interface on the new sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="30778-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="30778-111">Remarks</span></span>

<span data-ttu-id="30778-112">Questo metodo recupera un buffer vuoto dall'allocatore downstream.</span><span class="sxs-lookup"><span data-stu-id="30778-112">This method retrieves an empty buffer from the downstream allocator.</span></span> <span data-ttu-id="30778-113">Copia tutte le proprietà di esempio da *pSource* al nuovo esempio, insieme ai dati effettivi nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="30778-113">It copies all of the sample properties from *pSource* into the new sample, along with the actual data in the sample.</span></span> <span data-ttu-id="30778-114">Se il filtro usa due allocatori, chiama questo metodo per copiare i dati tra i buffer.</span><span class="sxs-lookup"><span data-stu-id="30778-114">If the filter is using two allocators, it calls this method to copy data across buffers.</span></span>

## <a name="requirements"></a><span data-ttu-id="30778-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30778-115">Requirements</span></span>



| <span data-ttu-id="30778-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="30778-116">Requirement</span></span> | <span data-ttu-id="30778-117">Valore</span><span class="sxs-lookup"><span data-stu-id="30778-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30778-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="30778-118">Header</span></span><br/>  | <dl> <span data-ttu-id="30778-119"><dt>Transip. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30778-119"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="30778-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="30778-120">Library</span></span><br/> | <dl> <span data-ttu-id="30778-121"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="30778-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30778-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30778-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30778-123">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="30778-123">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




