---
title: Funzione Updatesubresources con (stack-allocating) (D3dx12. h)
description: Aggiorna le sottorisorse con un'implementazione di allocazione dello stack.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 237e7df26b35b4cb5b1dba7b2a80c1baaac64e8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322382"
---
# <a name="updatesubresources-stack-allocating-function"></a><span data-ttu-id="57a00-104">Funzione Updatesubresources con (stack-allocazione)</span><span class="sxs-lookup"><span data-stu-id="57a00-104">UpdateSubresources (stack-allocating) function</span></span>

<span data-ttu-id="57a00-105">Aggiorna le sottorisorse con un'implementazione di allocazione dello stack.</span><span class="sxs-lookup"><span data-stu-id="57a00-105">Updates subresources with a stack-allocating implementation.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a00-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="57a00-106">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="57a00-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="57a00-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a00-108">*pCmdList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57a00-108">*pCmdList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a00-109">Tipo: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span><span class="sxs-lookup"><span data-stu-id="57a00-109">Type: **[**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***</span></span>

<span data-ttu-id="57a00-110">Elenco di comandi, come puntatore a un [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span><span class="sxs-lookup"><span data-stu-id="57a00-110">The command list, as a pointer to an [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist).</span></span>

</dd> <dt>

<span data-ttu-id="57a00-111">*pDestinationResource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57a00-111">*pDestinationResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a00-112">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="57a00-112">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="57a00-113">Risorsa di destinazione, come puntatore a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="57a00-113">The destination resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="57a00-114">*pIntermediate* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57a00-114">*pIntermediate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a00-115">Tipo: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span><span class="sxs-lookup"><span data-stu-id="57a00-115">Type: **[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***</span></span>

<span data-ttu-id="57a00-116">Risorsa intermedia, come puntatore a un [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="57a00-116">The intermediate resource, as a pointer to an [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span>

</dd> <dt>

<span data-ttu-id="57a00-117">*IntermediateOffset*</span><span class="sxs-lookup"><span data-stu-id="57a00-117">*IntermediateOffset*</span></span> 
</dt> <dd>

<span data-ttu-id="57a00-118">Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="57a00-118">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="57a00-119">Offset, in byte, della risorsa intermedia.</span><span class="sxs-lookup"><span data-stu-id="57a00-119">The offset, in bytes, to the intermediate resource.</span></span>

</dd> <dt>

<span data-ttu-id="57a00-120">*FirstSubresource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57a00-120">*FirstSubresource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a00-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="57a00-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="57a00-122">Indice della prima sottorisorsa nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="57a00-122">The index of the first subresource in the resource.</span></span> <span data-ttu-id="57a00-123">I valori validi sono compresi tra 0 e *MaxSubresources*.</span><span class="sxs-lookup"><span data-stu-id="57a00-123">Valid values range from 0 to *MaxSubresources*.</span></span>

</dd> <dt>

<span data-ttu-id="57a00-124">*NumSubresources* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57a00-124">*NumSubresources* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a00-125">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="57a00-125">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="57a00-126">Numero di sottorisorse nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="57a00-126">The number of subresources in the resource.</span></span> <span data-ttu-id="57a00-127">I valori validi sono compresi tra 1 e (*MaxSubresources*  -  *FirstSubresource*).</span><span class="sxs-lookup"><span data-stu-id="57a00-127">Valid values range from 1 to (*MaxSubresources* - *FirstSubresource*).</span></span>

</dd> <dt>

<span data-ttu-id="57a00-128">*pSrcData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57a00-128">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a00-129">Tipo: **[ **D3D12 \_ subresource \_ Data**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span><span class="sxs-lookup"><span data-stu-id="57a00-129">Type: **[**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***</span></span>

<span data-ttu-id="57a00-130">Puntatore a una matrice (di lunghezza *NumSubresources*) di puntatori alle strutture di [**\_ \_ dati della sottorisorsa D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) contenenti le descrizioni dei dati della sottorisorsa utilizzati per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="57a00-130">Pointer to an array (of length *NumSubresources*) of pointers to [**D3D12\_SUBRESOURCE\_DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) structures containing descriptions of the subresource data used for the update.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a00-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57a00-131">Return value</span></span>

<span data-ttu-id="57a00-132">Tipo: **[ **UInt64**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="57a00-132">Type: **[**UINT64**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="57a00-133">Dimensione del buffer, in byte.</span><span class="sxs-lookup"><span data-stu-id="57a00-133">The size, in bytes, of the buffer.</span></span>

## <a name="remarks"></a><span data-ttu-id="57a00-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="57a00-134">Remarks</span></span>

<span data-ttu-id="57a00-135">La dichiarazione di questa funzione inizia con: `template <UINT MaxSubresources>`</span><span class="sxs-lookup"><span data-stu-id="57a00-135">The declaration of this function begins with: `template <UINT MaxSubresources>`</span></span>

## <a name="requirements"></a><span data-ttu-id="57a00-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="57a00-136">Requirements</span></span>



| <span data-ttu-id="57a00-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a00-137">Requirement</span></span> | <span data-ttu-id="57a00-138">Valore</span><span class="sxs-lookup"><span data-stu-id="57a00-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57a00-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="57a00-139">Header</span></span><br/>  | <dl> <span data-ttu-id="57a00-140"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="57a00-140"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="57a00-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="57a00-141">Library</span></span><br/> | <dl> <span data-ttu-id="57a00-142"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="57a00-142"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="57a00-143">DLL</span><span class="sxs-lookup"><span data-stu-id="57a00-143">DLL</span></span><br/>     | <dl> <span data-ttu-id="57a00-144"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57a00-144"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a00-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="57a00-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a00-146">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="57a00-146">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="57a00-147">Sottorisorse</span><span class="sxs-lookup"><span data-stu-id="57a00-147">Subresources</span></span>](subresources.md)
</dt> </dl>

 

