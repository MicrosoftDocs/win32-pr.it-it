---
title: Interfaccia ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Un'interfaccia della variabile di matrice accede a una matrice.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11
- Interfaccia ID3DX11EffectMatrixVariable Direct3D 11, descritta
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5c4c89a231d429fc0a1f8fecbcbb4d06db35cb5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982367"
---
# <a name="id3dx11effectmatrixvariable-interface"></a><span data-ttu-id="3af97-105">Interfaccia ID3DX11EffectMatrixVariable</span><span class="sxs-lookup"><span data-stu-id="3af97-105">ID3DX11EffectMatrixVariable interface</span></span>

<span data-ttu-id="3af97-106">Un'interfaccia della variabile di matrice accede a una matrice.</span><span class="sxs-lookup"><span data-stu-id="3af97-106">A matrix-variable interface accesses a matrix.</span></span>

## <a name="members"></a><span data-ttu-id="3af97-107">Membri</span><span class="sxs-lookup"><span data-stu-id="3af97-107">Members</span></span>

<span data-ttu-id="3af97-108">L'interfaccia **ID3DX11EffectMatrixVariable** eredita da [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="3af97-108">The **ID3DX11EffectMatrixVariable** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="3af97-109">**ID3DX11EffectMatrixVariable** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3af97-109">**ID3DX11EffectMatrixVariable** also has these types of members:</span></span>

-   [<span data-ttu-id="3af97-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="3af97-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3af97-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="3af97-111">Methods</span></span>

<span data-ttu-id="3af97-112">L'interfaccia **ID3DX11EffectMatrixVariable** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="3af97-112">The **ID3DX11EffectMatrixVariable** interface has these methods.</span></span>



| <span data-ttu-id="3af97-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="3af97-113">Method</span></span>                                                                                 | <span data-ttu-id="3af97-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3af97-114">Description</span></span>                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="3af97-115">**GetMatrix**</span><span class="sxs-lookup"><span data-stu-id="3af97-115">**GetMatrix**</span></span>](id3dx11effectmatrixvariable-getmatrix.md)                             | <span data-ttu-id="3af97-116">Ottenere una matrice.</span><span class="sxs-lookup"><span data-stu-id="3af97-116">Get a matrix.</span></span><br/>                                          |
| [<span data-ttu-id="3af97-117">**GetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="3af97-117">**GetMatrixArray**</span></span>](id3dx11effectmatrixvariable-getmatrixarray.md)                   | <span data-ttu-id="3af97-118">Ottenere una matrice di matrici.</span><span class="sxs-lookup"><span data-stu-id="3af97-118">Get an array of matrices.</span></span><br/>                              |
| [<span data-ttu-id="3af97-119">**GetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="3af97-119">**GetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | <span data-ttu-id="3af97-120">Trasporre e ottenere una matrice a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3af97-120">Transpose and get a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="3af97-121">**GetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="3af97-121">**GetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | <span data-ttu-id="3af97-122">Trasporre e ottenere una matrice di matrici a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3af97-122">Transpose and get an array of floating-point matrices.</span></span><br/> |
| [<span data-ttu-id="3af97-123">**Sematrix**</span><span class="sxs-lookup"><span data-stu-id="3af97-123">**SetMatrix**</span></span>](id3dx11effectmatrixvariable-setmatrix.md)                             | <span data-ttu-id="3af97-124">Impostare una matrice a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3af97-124">Set a floating-point matrix.</span></span><br/>                           |
| [<span data-ttu-id="3af97-125">**SetMatrixArray**</span><span class="sxs-lookup"><span data-stu-id="3af97-125">**SetMatrixArray**</span></span>](id3dx11effectmatrixvariable-setmatrixarray.md)                   | <span data-ttu-id="3af97-126">Impostare una matrice di matrici a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3af97-126">Set an array of floating-point matrices.</span></span><br/>               |
| [<span data-ttu-id="3af97-127">**SetMatrixTranspose**</span><span class="sxs-lookup"><span data-stu-id="3af97-127">**SetMatrixTranspose**</span></span>](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | <span data-ttu-id="3af97-128">Trasponi e imposta una matrice a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3af97-128">Transpose and set a floating-point matrix.</span></span><br/>             |
| [<span data-ttu-id="3af97-129">**SetMatrixTransposeArray**</span><span class="sxs-lookup"><span data-stu-id="3af97-129">**SetMatrixTransposeArray**</span></span>](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | <span data-ttu-id="3af97-130">Trasponi e imposta una matrice di matrici a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="3af97-130">Transpose and set an array of floating-point matrices.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3af97-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="3af97-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3af97-132">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="3af97-132">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="3af97-133">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="3af97-133">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="3af97-134">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="3af97-134">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3af97-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3af97-135">Requirements</span></span>



| <span data-ttu-id="3af97-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3af97-136">Requirement</span></span> | <span data-ttu-id="3af97-137">Valore</span><span class="sxs-lookup"><span data-stu-id="3af97-137">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3af97-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3af97-138">Header</span></span><br/>  | <dl> <span data-ttu-id="3af97-139"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="3af97-139"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="3af97-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="3af97-140">Library</span></span><br/> | <dl> <span data-ttu-id="3af97-141"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="3af97-141"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3af97-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3af97-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3af97-143">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="3af97-143">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="3af97-144">Interfacce Effects 11</span><span class="sxs-lookup"><span data-stu-id="3af97-144">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3af97-145">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="3af97-145">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





