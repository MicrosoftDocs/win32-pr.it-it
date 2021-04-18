---
description: Recupera le opzioni di mesh abilitate per questa mesh al momento della creazione.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'Metodo ID3DXBaseMesh:: GetOptions (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323219"
---
# <a name="id3dxbasemeshgetoptions-method"></a><span data-ttu-id="3d17e-103">Metodo ID3DXBaseMesh:: GetOptions</span><span class="sxs-lookup"><span data-stu-id="3d17e-103">ID3DXBaseMesh::GetOptions method</span></span>

<span data-ttu-id="3d17e-104">Recupera le opzioni di mesh abilitate per questa mesh al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3d17e-104">Retrieves the mesh options enabled for this mesh at creation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d17e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3d17e-105">Syntax</span></span>


```C++
DWORD GetOptions();
```



## <a name="parameters"></a><span data-ttu-id="3d17e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3d17e-106">Parameters</span></span>

<span data-ttu-id="3d17e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="3d17e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d17e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3d17e-108">Return value</span></span>

<span data-ttu-id="3d17e-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3d17e-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3d17e-110">Restituisce una combinazione di uno o più dei flag seguenti, che indica le opzioni abilitate per la mesh al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="3d17e-110">Returns a combination of one or more of the following flags, indicating the options enabled for this mesh at creation time.</span></span>



| <span data-ttu-id="3d17e-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3d17e-111">Value</span></span>                   | <span data-ttu-id="3d17e-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3d17e-112">Description</span></span>                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d17e-113">D3DXMESH a \_ 32 bit</span><span class="sxs-lookup"><span data-stu-id="3d17e-113">D3DXMESH\_32BIT</span></span>         | <span data-ttu-id="3d17e-114">Usare gli indici a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="3d17e-114">Use 32-bit indices.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="3d17e-115">\_DONOTCLIP D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="3d17e-115">D3DXMESH\_DONOTCLIP</span></span>     | <span data-ttu-id="3d17e-116">Usare il \_ flag di utilizzo di DONOTCLIP D3DUSAGE per i buffer di Vertex e index.</span><span class="sxs-lookup"><span data-stu-id="3d17e-116">Use the D3DUSAGE\_DONOTCLIP usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="3d17e-117">D3DXMESH \_ dinamico</span><span class="sxs-lookup"><span data-stu-id="3d17e-117">D3DXMESH\_DYNAMIC</span></span>       | <span data-ttu-id="3d17e-118">Equivale a specificare D3DXMESH \_ VB \_ Dynamic e D3DXMESH \_ IB \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="3d17e-118">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>                                                                                                                   |
| <span data-ttu-id="3d17e-119">\_RTPATCHES D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="3d17e-119">D3DXMESH\_RTPATCHES</span></span>     | <span data-ttu-id="3d17e-120">Usare il \_ flag di utilizzo di RTPATCHES D3DUSAGE per i buffer di Vertex e index.</span><span class="sxs-lookup"><span data-stu-id="3d17e-120">Use the D3DUSAGE\_RTPATCHES usage flag for vertex and index buffers.</span></span>                                                                                                                             |
| <span data-ttu-id="3d17e-121">\_NPATCHES D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="3d17e-121">D3DXMESH\_NPATCHES</span></span>      | <span data-ttu-id="3d17e-122">Se si specifica questo flag, il vertice e il buffer dell'indice della mesh verranno creati con il \_ flag D3DUSAGE NPATCHES.</span><span class="sxs-lookup"><span data-stu-id="3d17e-122">Specifying this flag causes the vertex and index buffer of the mesh to be created with D3DUSAGE\_NPATCHES flag.</span></span> <span data-ttu-id="3d17e-123">Questa operazione è obbligatoria se è necessario eseguire il rendering dell'oggetto mesh usando la funzionalità di miglioramento della patch N.</span><span class="sxs-lookup"><span data-stu-id="3d17e-123">This is required if the mesh object is to be rendered using N-Patch enhancement.</span></span> |
| <span data-ttu-id="3d17e-124">D3DXMESH \_ gestito</span><span class="sxs-lookup"><span data-stu-id="3d17e-124">D3DXMESH\_MANAGED</span></span>       | <span data-ttu-id="3d17e-125">Equivale a specificare sia \_ gestito D3DXMESH VB \_ che D3DXMESH \_ IB \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="3d17e-125">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>                                                                                                                   |
| <span data-ttu-id="3d17e-126">\_Punti D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="3d17e-126">D3DXMESH\_POINTS</span></span>        | <span data-ttu-id="3d17e-127">Usare il \_ flag di utilizzo dei punti di D3DUSAGE per i buffer dei vertici e degli indici.</span><span class="sxs-lookup"><span data-stu-id="3d17e-127">Use the D3DUSAGE\_POINTS usage flag for vertex and index buffers.</span></span>                                                                                                                                |
| <span data-ttu-id="3d17e-128">D3DXMESH \_ IB \_ dinamico</span><span class="sxs-lookup"><span data-stu-id="3d17e-128">D3DXMESH\_IB\_DYNAMIC</span></span>   | <span data-ttu-id="3d17e-129">Usare il \_ flag di utilizzo dinamico D3DUSAGE per i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="3d17e-129">Use the D3DUSAGE\_DYNAMIC usage flag for index buffers.</span></span>                                                                                                                                          |
| <span data-ttu-id="3d17e-130">D3DXMESH \_ IB \_ gestito</span><span class="sxs-lookup"><span data-stu-id="3d17e-130">D3DXMESH\_IB\_MANAGED</span></span>   | <span data-ttu-id="3d17e-131">Usare la \_ classe di memoria gestita D3DPOOL per i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="3d17e-131">Use the D3DPOOL\_MANAGED memory class for index buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="3d17e-132">D3DXMESH \_ IB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="3d17e-132">D3DXMESH\_IB\_SYSTEMMEM</span></span> | <span data-ttu-id="3d17e-133">Usare la \_ classe D3DPOOL SYSTEMMEM Memory per i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="3d17e-133">Use the D3DPOOL\_SYSTEMMEM memory class for index buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="3d17e-134">D3DXMESH \_ IB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="3d17e-134">D3DXMESH\_IB\_WRITEONLY</span></span> | <span data-ttu-id="3d17e-135">Usare il \_ flag di utilizzo di D3DUSAGE WRITEONLY per i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="3d17e-135">Use the D3DUSAGE\_WRITEONLY usage flag for index buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="3d17e-136">\_SYSTEMMEM D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="3d17e-136">D3DXMESH\_SYSTEMMEM</span></span>     | <span data-ttu-id="3d17e-137">Equivale a specificare sia D3DXMESH \_ VB \_ SYSTEMMEM che D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="3d17e-137">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>                                                                                                               |
| <span data-ttu-id="3d17e-138">D3DXMESH \_ VB \_ dinamico</span><span class="sxs-lookup"><span data-stu-id="3d17e-138">D3DXMESH\_VB\_DYNAMIC</span></span>   | <span data-ttu-id="3d17e-139">Usare il \_ flag di utilizzo dinamico D3DUSAGE per i buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="3d17e-139">Use the D3DUSAGE\_DYNAMIC usage flag for vertex buffers.</span></span>                                                                                                                                         |
| <span data-ttu-id="3d17e-140">D3DXMESH \_ VB \_ gestito</span><span class="sxs-lookup"><span data-stu-id="3d17e-140">D3DXMESH\_VB\_MANAGED</span></span>   | <span data-ttu-id="3d17e-141">Usare la \_ classe di memoria gestita D3DPOOL per i buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="3d17e-141">Use the D3DPOOL\_MANAGED memory class for vertex buffers.</span></span>                                                                                                                                        |
| <span data-ttu-id="3d17e-142">D3DXMESH \_ VB \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="3d17e-142">D3DXMESH\_VB\_SYSTEMMEM</span></span> | <span data-ttu-id="3d17e-143">Usare la \_ classe D3DPOOL SYSTEMMEM Memory per i buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="3d17e-143">Use the D3DPOOL\_SYSTEMMEM memory class for vertex buffers.</span></span>                                                                                                                                      |
| <span data-ttu-id="3d17e-144">D3DXMESH \_ VB \_ WRITEONLY</span><span class="sxs-lookup"><span data-stu-id="3d17e-144">D3DXMESH\_VB\_WRITEONLY</span></span> | <span data-ttu-id="3d17e-145">Usare il \_ flag di utilizzo di D3DUSAGE WRITEONLY per i buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="3d17e-145">Use the D3DUSAGE\_WRITEONLY usage flag for vertex buffers.</span></span>                                                                                                                                       |
| <span data-ttu-id="3d17e-146">\_WRITEONLY D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="3d17e-146">D3DXMESH\_WRITEONLY</span></span>     | <span data-ttu-id="3d17e-147">Equivale a specificare sia D3DXMESH \_ VB \_ WRITEONLY che D3DXMESH \_ IB \_ WRITEONLY.</span><span class="sxs-lookup"><span data-stu-id="3d17e-147">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>                                                                                                               |



 

## <a name="requirements"></a><span data-ttu-id="3d17e-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d17e-148">Requirements</span></span>



| <span data-ttu-id="3d17e-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d17e-149">Requirement</span></span> | <span data-ttu-id="3d17e-150">Valore</span><span class="sxs-lookup"><span data-stu-id="3d17e-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d17e-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d17e-151">Header</span></span><br/>  | <dl> <span data-ttu-id="3d17e-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d17e-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3d17e-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="3d17e-153">Library</span></span><br/> | <dl> <span data-ttu-id="3d17e-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3d17e-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3d17e-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d17e-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d17e-156">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="3d17e-156">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
