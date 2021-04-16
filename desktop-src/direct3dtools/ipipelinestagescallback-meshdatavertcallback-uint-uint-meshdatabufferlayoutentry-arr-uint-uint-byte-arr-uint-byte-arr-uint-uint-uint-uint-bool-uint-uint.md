---
description: Callback che notifica all'host delle fasi della pipeline le informazioni mesh restituite dalla richiesta associata.
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IPipeLineStagesCallback:: MeshDataVertCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521386"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span data-ttu-id="670b0-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>Metodo IPipeLineStagesCallback:: MeshDataVertCallback</span><span class="sxs-lookup"><span data-stu-id="670b0-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback::MeshDataVertCallback method</span></span>

<span data-ttu-id="670b0-104">Callback che notifica all'host delle fasi della pipeline le informazioni mesh restituite dalla richiesta associata.</span><span class="sxs-lookup"><span data-stu-id="670b0-104">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="670b0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="670b0-105">Syntax</span></span>


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a><span data-ttu-id="670b0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="670b0-106">Parameters</span></span>

<span data-ttu-id="670b0-107">*numVertices* </span><span class="sxs-lookup"><span data-stu-id="670b0-107">*numVertices* </span></span>  
<span data-ttu-id="670b0-108">Numero di vertici nei risultati.</span><span class="sxs-lookup"><span data-stu-id="670b0-108">The number of vertices in the results.</span></span>

<span data-ttu-id="670b0-109">*numBufferLayoutEntries* </span><span class="sxs-lookup"><span data-stu-id="670b0-109">*numBufferLayoutEntries* </span></span>  
<span data-ttu-id="670b0-110">Numero di voci del layout del buffer nei risultati.</span><span class="sxs-lookup"><span data-stu-id="670b0-110">The number of buffer layout entries in the results.</span></span>

<span data-ttu-id="670b0-111">*voci di count1 \_* </span><span class="sxs-lookup"><span data-stu-id="670b0-111">*count1\_entries* </span></span>  
<span data-ttu-id="670b0-112">Il layout del buffer è intero.</span><span class="sxs-lookup"><span data-stu-id="670b0-112">The buffer layout entires.</span></span> <span data-ttu-id="670b0-113">Che descrivono la firma di output dello shader.</span><span class="sxs-lookup"><span data-stu-id="670b0-113">These describe the shader output signature.</span></span>

<span data-ttu-id="670b0-114">*stride* </span><span class="sxs-lookup"><span data-stu-id="670b0-114">*stride* </span></span>  
<span data-ttu-id="670b0-115">Dimensione (stride) di un intero blocco di output.</span><span class="sxs-lookup"><span data-stu-id="670b0-115">The size (stride) of an entire output chunk.</span></span>

<span data-ttu-id="670b0-116">*numVBBytes* </span><span class="sxs-lookup"><span data-stu-id="670b0-116">*numVBBytes* </span></span>  
<span data-ttu-id="670b0-117">Dimensioni in byte del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="670b0-117">The size of the vertex buffer in bytes.</span></span>

<span data-ttu-id="670b0-118">*\_pVBData count4* </span><span class="sxs-lookup"><span data-stu-id="670b0-118">*count4\_pVBData* </span></span>  
<span data-ttu-id="670b0-119">Buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="670b0-119">The vertex buffer.</span></span>

<span data-ttu-id="670b0-120">*numIBBytes* </span><span class="sxs-lookup"><span data-stu-id="670b0-120">*numIBBytes* </span></span>  
<span data-ttu-id="670b0-121">Dimensioni in byte del buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="670b0-121">The size of the index buffer in bytes.</span></span>

<span data-ttu-id="670b0-122">*\_pIBData count6* </span><span class="sxs-lookup"><span data-stu-id="670b0-122">*count6\_pIBData* </span></span>  
<span data-ttu-id="670b0-123">Buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="670b0-123">The index buffer.</span></span>

<span data-ttu-id="670b0-124">*indexSize* </span><span class="sxs-lookup"><span data-stu-id="670b0-124">*indexSize* </span></span>  
<span data-ttu-id="670b0-125">Dimensioni in byte di ogni indice.</span><span class="sxs-lookup"><span data-stu-id="670b0-125">The size of each index in bytes.</span></span>

<span data-ttu-id="670b0-126">*IBOffset* </span><span class="sxs-lookup"><span data-stu-id="670b0-126">*IBOffset* </span></span>  
<span data-ttu-id="670b0-127">Offset nel buffer di indice che specifica la posizione in cui gli indici devono iniziare a essere utilizzati.</span><span class="sxs-lookup"><span data-stu-id="670b0-127">An offset into the index buffer that specifies where indices should start being used.</span></span>

<span data-ttu-id="670b0-128">*baseVertex* </span><span class="sxs-lookup"><span data-stu-id="670b0-128">*baseVertex* </span></span>  
<span data-ttu-id="670b0-129">Offset nel buffer dei vertici che specifica la posizione in cui iniziare a usare i vertici.</span><span class="sxs-lookup"><span data-stu-id="670b0-129">An offset into the vertex buffer that specifies where vertices should start being used.</span></span>

<span data-ttu-id="670b0-130">*minVertex*</span><span class="sxs-lookup"><span data-stu-id="670b0-130">*minVertex*</span></span>   

<span data-ttu-id="670b0-131">*IBIndexesVB* </span><span class="sxs-lookup"><span data-stu-id="670b0-131">*IBIndexesVB* </span></span>  
<span data-ttu-id="670b0-132">true quando viene utilizzato il buffer di indice; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="670b0-132">true when the index buffer is used; otherwise false.</span></span>

<span data-ttu-id="670b0-133">*numIndices* </span><span class="sxs-lookup"><span data-stu-id="670b0-133">*numIndices* </span></span>  
<span data-ttu-id="670b0-134">Numero di indici utilizzati.</span><span class="sxs-lookup"><span data-stu-id="670b0-134">The number of indices used.</span></span>

<span data-ttu-id="670b0-135">*topologia* </span><span class="sxs-lookup"><span data-stu-id="670b0-135">*topology* </span></span>  
<span data-ttu-id="670b0-136">Topolology dello shader.</span><span class="sxs-lookup"><span data-stu-id="670b0-136">The topolology of the shader.</span></span> <span data-ttu-id="670b0-137">Questa operazione non è necessariamente identica alla topologia della chiamata di progetto associata.</span><span class="sxs-lookup"><span data-stu-id="670b0-137">This is not necessarily the same as the topology of the associated draw call.</span></span>

## <a name="return-value"></a><span data-ttu-id="670b0-138">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="670b0-138">Return value</span></span>

<span data-ttu-id="670b0-139">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="670b0-139">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="670b0-140">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="670b0-140">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="670b0-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="670b0-141">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="670b0-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="670b0-142">Header</span></span></p></td><td><span data-ttu-id="670b0-143">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="670b0-143">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="670b0-144"><span id="see_also"></span>Vedere anche</span><span class="sxs-lookup"><span data-stu-id="670b0-144"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="670b0-145">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="670b0-145">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
