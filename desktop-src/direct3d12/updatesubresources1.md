---
title: Funzione Updatesubresources con (D3dx12. h)
description: Aggiorna le sottorisorse. tutte le matrici di risorse devono essere popolate, in genere chiamando ID3D12Device GetCopyableFootprints.
ms.assetid: D6885165-095E-452D-8D93-A2C43A215F48
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
ms.openlocfilehash: 885ee058aacbfca238448830f2b7b1b54a298f89
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323550"
---
# <a name="updatesubresources-function"></a><span data-ttu-id="58ebf-104">Updatesubresources con (funzione)</span><span class="sxs-lookup"><span data-stu-id="58ebf-104">UpdateSubresources function</span></span>

<span data-ttu-id="58ebf-105">Aggiorna le sottorisorse, tutte le matrici di sottorisorse devono essere popolate, in genere chiamando [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span><span class="sxs-lookup"><span data-stu-id="58ebf-105">Updates subresources, all the subresource arrays should be populated, typically by calling [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints).</span></span>

## <a name="syntax"></a><span data-ttu-id="58ebf-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58ebf-106">Syntax</span></span>


```C++
UINT64 inline UpdateSubresources(
  _In_       ID3D12GraphicsCommandList          *pCmdList,
  _In_       ID3D12Resource                     *pDestinationResource,
  _In_       ID3D12Resource                     *pIntermediate,
  _In_       UINT                               FirstSubresource,
  _In_       UINT                               NumSubresources,
             UINT64                             RequiredSize,
  _In_ const D3D12_PLACED_SUBRESOURCE_FOOTPRINT *pLayouts,
  _In_ const UINT                               *pNumRows,
  _In_ const UINT64                             *pRowSizesInBytes,
  _In_ const D3D12_SUBRESOURCE_DATA             *pSrcData
);
```



## <a name="parameters"></a><span data-ttu-id="58ebf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="58ebf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58ebf-108">*pCmdList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ebf-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ebf-109">Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="58ebf-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="58ebf-110">Elenco di comandi, come puntatore a un [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="58ebf-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="58ebf-111">*pDestinationResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ebf-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ebf-112">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="58ebf-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="58ebf-113">Risorsa di destinazione, come puntatore a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="58ebf-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="58ebf-114">*pIntermediate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ebf-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ebf-115">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="58ebf-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="58ebf-116">Risorsa intermedia, come puntatore a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="58ebf-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="58ebf-117">*FirstSubresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ebf-117">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ebf-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="58ebf-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="58ebf-119">Indice della prima sottorisorsa nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="58ebf-119">The index of the first subresource in the resource.</span></span> <span data-ttu-id="58ebf-120">L'intervallo di valori validi è compreso tra 0 e D3D12 le \_ \_ sottorisorse di req.</span><span class="sxs-lookup"><span data-stu-id="58ebf-120">The range of valid values is 0 to D3D12\_REQ\_SUBRESOURCES.</span></span>

</dd> <dt>

<span data-ttu-id="58ebf-121">*NumSubresources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ebf-121">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ebf-122">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="58ebf-122">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="58ebf-123">Numero di sottorisorse nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="58ebf-123">The number of subresources in the resource.</span></span> <span data-ttu-id="58ebf-124">L'intervallo di valori validi è compreso tra 0 e (D3D12 \_ req Resources \_ - *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="58ebf-124">The range of valid values is 0 to (D3D12\_REQ\_SUBRESOURCES - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="58ebf-125">*RequiredSize*</span><span class="sxs-lookup"><span data-stu-id="58ebf-125">*RequiredSize*</span></span> 
</dt> <dd>

<span data-ttu-id="58ebf-126">Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="58ebf-126">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="58ebf-127">Dimensioni richieste, in byte, per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="58ebf-127">The required size, in bytes, for the update.</span></span>

</dd> <dt>

<span data-ttu-id="58ebf-128">*pLayouts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ebf-128">*pLayouts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ebf-129">Tipo: **const \* [**D3D12 \_ POSIZIONAta \_ \_ footprint delle risorse**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)**</span><span class="sxs-lookup"><span data-stu-id="58ebf-129">Type: **const [**D3D12\_PLACED\_SUBRESOURCE\_FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)\***</span></span>

<span data-ttu-id="58ebf-130">Puntatore a una matrice (di lunghezza *NumSubresources*) di puntatori alle strutture che contengono la descrizione e il posizionamento delle sottorisorse della risorsa.</span><span class="sxs-lookup"><span data-stu-id="58ebf-130">Pointer to an array (of length *NumSubresources*) of pointers to the structures that contains the description and placement of the resource's subresources.</span></span>

</dd> <dt>

<span data-ttu-id="58ebf-131">*pNumRows* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ebf-131">*pNumRows* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ebf-132">Tipo: **const [**uint**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="58ebf-132">Type: **const [**UINT**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="58ebf-133">Puntatore a una matrice di lunghezza *NumSubresources* di uints contenente il numero di righe per ogni sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="58ebf-133">Pointer to an array (of length *NumSubresources*) of UINTS containing the number of rows for each subresource.</span></span>

</dd> <dt>

<span data-ttu-id="58ebf-134">*pRowSizesInBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ebf-134">*pRowSizesInBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ebf-135">Tipo: **const [**UInt64**](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="58ebf-135">Type: **const [**UINT64**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="58ebf-136">Puntatore a una matrice di lunghezza *NumSubresources* di uints che contiene la dimensione, in byte, di ogni riga.</span><span class="sxs-lookup"><span data-stu-id="58ebf-136">Pointer to an array (of length *NumSubresources*) of UINTS containing the size, in bytes, of each row.</span></span>

</dd> <dt>

<span data-ttu-id="58ebf-137">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58ebf-137">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58ebf-138">Tipo: **const \* [**D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)**</span><span class="sxs-lookup"><span data-stu-id="58ebf-138">Type: **const [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="58ebf-139">Puntatore a una matrice (di lunghezza *NumSubresources*) di puntatori alle strutture di [**\_ \_ dati della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenenti le descrizioni dei dati della sottorisorsa utilizzati per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="58ebf-139">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58ebf-140">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58ebf-140">Return value</span></span>

<span data-ttu-id="58ebf-141">Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="58ebf-141">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="58ebf-142">Dimensione del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="58ebf-142">The size, in bytes, of the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="58ebf-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58ebf-143">Requirements</span></span>



| <span data-ttu-id="58ebf-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="58ebf-144">Requirement</span></span> | <span data-ttu-id="58ebf-145">Valore</span><span class="sxs-lookup"><span data-stu-id="58ebf-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="58ebf-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58ebf-146">Header</span></span><br/>  | <dl> <span data-ttu-id="58ebf-147"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="58ebf-147"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="58ebf-148">Libreria</span><span class="sxs-lookup"><span data-stu-id="58ebf-148">Library</span></span><br/> | <dl> <span data-ttu-id="58ebf-149"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58ebf-149"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="58ebf-150">DLL</span><span class="sxs-lookup"><span data-stu-id="58ebf-150">DLL</span></span><br/>     | <dl> <span data-ttu-id="58ebf-151"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58ebf-151"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58ebf-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58ebf-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58ebf-153">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="58ebf-153">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="58ebf-154">Sottorisorse</span><span class="sxs-lookup"><span data-stu-id="58ebf-154">Subresources</span></span>](subresources.md)
</dt> </dl>

 

