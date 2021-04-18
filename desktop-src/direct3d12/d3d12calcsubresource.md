---
title: Funzione D3D12CalcSubresource (D3dx12. h)
description: Calcola un indice di una sottorisorsa per una trama.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource (funzione)
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322180"
---
# <a name="d3d12calcsubresource-function"></a><span data-ttu-id="97c90-104">D3D12CalcSubresource (funzione)</span><span class="sxs-lookup"><span data-stu-id="97c90-104">D3D12CalcSubresource function</span></span>

<span data-ttu-id="97c90-105">Calcola un indice di una sottorisorsa per una trama.</span><span class="sxs-lookup"><span data-stu-id="97c90-105">Calculates a subresource index for a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c90-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97c90-106">Syntax</span></span>


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a><span data-ttu-id="97c90-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="97c90-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c90-108">*MipSlice*</span><span class="sxs-lookup"><span data-stu-id="97c90-108">*MipSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="97c90-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97c90-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97c90-110">Indice in base zero per il livello mipmap da indirizzare; 0 indica il primo livello di mipmap più dettagliato.</span><span class="sxs-lookup"><span data-stu-id="97c90-110">The zero-based index for the mipmap level to address; 0 indicates the first, most detailed mipmap level.</span></span>

</dd> <dt>

<span data-ttu-id="97c90-111">*ArraySlice*</span><span class="sxs-lookup"><span data-stu-id="97c90-111">*ArraySlice*</span></span> 
</dt> <dd>

<span data-ttu-id="97c90-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97c90-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97c90-113">Indice in base zero per il livello di matrice da indirizzare. usare sempre 0 per le trame del volume (3D).</span><span class="sxs-lookup"><span data-stu-id="97c90-113">The zero-based index for the array level to address; always use 0 for volume (3D) textures.</span></span>

</dd> <dt>

<span data-ttu-id="97c90-114">*PlaneSlice*</span><span class="sxs-lookup"><span data-stu-id="97c90-114">*PlaneSlice*</span></span> 
</dt> <dd>

<span data-ttu-id="97c90-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97c90-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97c90-116">Indice in base zero per il livello del piano da indirizzare.</span><span class="sxs-lookup"><span data-stu-id="97c90-116">The zero-based index for the plane level to address.</span></span>

</dd> <dt>

<span data-ttu-id="97c90-117">*MipLevels*</span><span class="sxs-lookup"><span data-stu-id="97c90-117">*MipLevels*</span></span> 
</dt> <dd>

<span data-ttu-id="97c90-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97c90-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97c90-119">Il numero di livelli di mipmap nella risorsa.</span><span class="sxs-lookup"><span data-stu-id="97c90-119">The number of mipmap levels in the resource.</span></span>

</dd> <dt>

<span data-ttu-id="97c90-120">*ArraySize*</span><span class="sxs-lookup"><span data-stu-id="97c90-120">*ArraySize*</span></span> 
</dt> <dd>

<span data-ttu-id="97c90-121">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97c90-121">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97c90-122">Numero di elementi nella matrice.</span><span class="sxs-lookup"><span data-stu-id="97c90-122">The number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c90-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97c90-123">Return value</span></span>

<span data-ttu-id="97c90-124">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97c90-124">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97c90-125">Indice che equivale a MipSlice + (ArraySlice \* MipLevels).</span><span class="sxs-lookup"><span data-stu-id="97c90-125">The index which equals MipSlice + (ArraySlice \* MipLevels).</span></span>

## <a name="remarks"></a><span data-ttu-id="97c90-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="97c90-126">Remarks</span></span>

<span data-ttu-id="97c90-127">Un buffer è una risorsa non strutturata e pertanto viene definito come contenente una singola sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="97c90-127">A buffer is an unstructured resource and is therefore defined as containing a single subresource.</span></span> <span data-ttu-id="97c90-128">Le API che accettano i buffer non necessitano di un indice di sottorisorse.</span><span class="sxs-lookup"><span data-stu-id="97c90-128">APIs that take buffers do not need a subresource index.</span></span> <span data-ttu-id="97c90-129">Un trame d'altra parte è altamente strutturato.</span><span class="sxs-lookup"><span data-stu-id="97c90-129">A texture on the other hand is highly structured.</span></span> <span data-ttu-id="97c90-130">Ogni oggetto texture può contenere una o più sottorisorse in base alle dimensioni della matrice e al numero di livelli di mipmap.</span><span class="sxs-lookup"><span data-stu-id="97c90-130">Each texture object may contain one or more subresources depending on the size of the array and the number of mipmap levels.</span></span>

<span data-ttu-id="97c90-131">Per le trame volume (3D), tutte le sezioni per un determinato livello di mipmap sono un singolo indice di sottorisorsa.</span><span class="sxs-lookup"><span data-stu-id="97c90-131">For volume (3D) textures, all slices for a given mipmap level are a single subresource index.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c90-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97c90-132">Requirements</span></span>



| <span data-ttu-id="97c90-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c90-133">Requirement</span></span> | <span data-ttu-id="97c90-134">Valore</span><span class="sxs-lookup"><span data-stu-id="97c90-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97c90-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97c90-135">Header</span></span><br/>  | <dl> <span data-ttu-id="97c90-136"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="97c90-136"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="97c90-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="97c90-137">Library</span></span><br/> | <dl> <span data-ttu-id="97c90-138"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="97c90-138"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="97c90-139">DLL</span><span class="sxs-lookup"><span data-stu-id="97c90-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="97c90-140"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97c90-140"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c90-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97c90-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c90-142">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="97c90-142">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="97c90-143">Sottorisorse</span><span class="sxs-lookup"><span data-stu-id="97c90-143">Subresources</span></span>](subresources.md)
</dt> </dl>

 

