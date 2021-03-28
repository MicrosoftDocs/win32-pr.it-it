---
title: Metodo ID3DX11Effect GetClassLinkage (D3dx11effect. h)
description: Ottiene un'interfaccia di collegamento di classe.
ms.assetid: 006c900d-3464-4666-9fe9-d62ba8cb2b7f
keywords:
- Metodo GetClassLinkage Direct3D 11
- Metodo GetClassLinkage Direct3D 11, interfaccia ID3DX11Effect
- Interfaccia ID3DX11Effect Direct3D 11, metodo GetClassLinkage
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetClassLinkage
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b19f14794186f85d0a51f21bc6b2759e512998
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969323"
---
# <a name="id3dx11effectgetclasslinkage-method"></a><span data-ttu-id="86cc3-106">Metodo ID3DX11Effect:: GetClassLinkage</span><span class="sxs-lookup"><span data-stu-id="86cc3-106">ID3DX11Effect::GetClassLinkage method</span></span>

<span data-ttu-id="86cc3-107">Ottiene un'interfaccia di collegamento di classe.</span><span class="sxs-lookup"><span data-stu-id="86cc3-107">Gets a class linkage interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="86cc3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86cc3-108">Syntax</span></span>


```C++
ID3D11ClassLinkage* GetClassLinkage();
```



## <a name="parameters"></a><span data-ttu-id="86cc3-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="86cc3-109">Parameters</span></span>

<span data-ttu-id="86cc3-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="86cc3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86cc3-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86cc3-111">Return value</span></span>

<span data-ttu-id="86cc3-112">Tipo: **[ **ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span><span class="sxs-lookup"><span data-stu-id="86cc3-112">Type: **[**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage)\***</span></span>

<span data-ttu-id="86cc3-113">Restituisce un puntatore a un'interfaccia [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) .</span><span class="sxs-lookup"><span data-stu-id="86cc3-113">Returns a pointer to an [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="86cc3-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="86cc3-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="86cc3-115">DirectX SDK non fornisce binari compilati per gli effetti.</span><span class="sxs-lookup"><span data-stu-id="86cc3-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="86cc3-116">È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects.</span><span class="sxs-lookup"><span data-stu-id="86cc3-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="86cc3-117">Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="86cc3-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="86cc3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86cc3-118">Requirements</span></span>



| <span data-ttu-id="86cc3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="86cc3-119">Requirement</span></span> | <span data-ttu-id="86cc3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="86cc3-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86cc3-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86cc3-121">Header</span></span><br/>  | <dl> <span data-ttu-id="86cc3-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="86cc3-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="86cc3-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="86cc3-123">Library</span></span><br/> | <dl> <span data-ttu-id="86cc3-124"><dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt></span><span class="sxs-lookup"><span data-stu-id="86cc3-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86cc3-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86cc3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86cc3-126">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="86cc3-126">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

 





