---
title: Funzione Updatesubresources con (allocazione heap) (D3dx12. h)
description: Aggiorna le sottorisorse con un'implementazione di allocazione dell'heap.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
keywords:
- Updatesubresources con (funzione)
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97abe59bdd0334fe4b7badf03e44ddc03b85495
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322896"
---
# <a name="updatesubresources-heap-allocating-function"></a><span data-ttu-id="b43d7-104">Funzione Updatesubresources con (allocazione heap)</span><span class="sxs-lookup"><span data-stu-id="b43d7-104">UpdateSubresources (heap-allocating) function</span></span>

<span data-ttu-id="b43d7-105">Aggiorna le sottorisorse con un'implementazione di allocazione dell'heap.</span><span class="sxs-lookup"><span data-stu-id="b43d7-105">Updates subresources with a heap-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b43d7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b43d7-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="b43d7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b43d7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b43d7-108">*pCmdList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b43d7-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b43d7-109">Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="b43d7-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="b43d7-110">Puntatore all'interfaccia [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) per l'elenco dei comandi.</span><span class="sxs-lookup"><span data-stu-id="b43d7-110">A pointer to the [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) interface for the command list.</span></span>

</dd> <dt>

<span data-ttu-id="b43d7-111">*pDestinationResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b43d7-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b43d7-112">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="b43d7-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="b43d7-113">Puntatore all'interfaccia [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) che rappresenta la risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b43d7-113">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the destination resource.</span></span>

</dd> <dt>

<span data-ttu-id="b43d7-114">*pIntermediate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b43d7-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b43d7-115">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="b43d7-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="b43d7-116">Puntatore all'interfaccia [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) che rappresenta la risorsa intermedia.</span><span class="sxs-lookup"><span data-stu-id="b43d7-116">A pointer to the [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) interface that represents the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="b43d7-117">*IntermediateOffset*</span><span class="sxs-lookup"><span data-stu-id="b43d7-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="b43d7-118">Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b43d7-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b43d7-119">Offset, in byte, della risorsa intermedia.</span><span class="sxs-lookup"><span data-stu-id="b43d7-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="b43d7-120">*FirstSubresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b43d7-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b43d7-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b43d7-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b43d7-122">Indice della prima sottorisorsa nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="b43d7-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="b43d7-123">L'intervallo di valori validi è compreso tra 0 e D3D12 le \_ \_ sottorisorse di req.</span><span class="sxs-lookup"><span data-stu-id="b43d7-123">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="b43d7-124">*NumSubresources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b43d7-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b43d7-125">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b43d7-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b43d7-126">Numero di sottorisorse nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="b43d7-126">The number of subresources in the resource.</span></span> <span data-ttu-id="b43d7-127">L'intervallo di valori validi è compreso tra 0 e (D3D12 \_ req Resources \_ - *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="b43d7-127">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="b43d7-128">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b43d7-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b43d7-129">Tipo: **[ **D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="b43d7-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="b43d7-130">Puntatore a una matrice (di lunghezza *NumSubresources*) di puntatori alle strutture di [**\_ \_ dati della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenenti le descrizioni dei dati della sottorisorsa utilizzati per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b43d7-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b43d7-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b43d7-131">Return value</span></span>

<span data-ttu-id="b43d7-132">Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b43d7-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b43d7-133">Dimensione del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="b43d7-133">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="b43d7-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b43d7-134">Requirements</span></span>



| <span data-ttu-id="b43d7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="b43d7-135">Requirement</span></span> | <span data-ttu-id="b43d7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="b43d7-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b43d7-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b43d7-137">Header</span></span><br/>  | <dl> <span data-ttu-id="b43d7-138"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="b43d7-138"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="b43d7-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="b43d7-139">Library</span></span><br/> | <dl> <span data-ttu-id="b43d7-140"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b43d7-140"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="b43d7-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b43d7-141">DLL</span></span><br/>     | <dl> <span data-ttu-id="b43d7-142"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b43d7-142"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b43d7-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b43d7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b43d7-144">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="b43d7-144">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="b43d7-145">Sottorisorse</span><span class="sxs-lookup"><span data-stu-id="b43d7-145">Subresources</span></span>](subresources.md)
</dt> </dl>

 

