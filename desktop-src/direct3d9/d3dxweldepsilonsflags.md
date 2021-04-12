---
description: Opzioni per la saldatura dei vertici.
ms.assetid: e73af63d-ed02-4fbc-8386-e8a40b0465ea
title: Enumerazione D3DXWELDEPSILONSFLAGS (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXWELDEPSILONSFLAGS
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 9e67c8b0f0bf93c9da181a5bba9a694525bd9819
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355039"
---
# <a name="d3dxweldepsilonsflags-enumeration"></a><span data-ttu-id="2324c-103">Enumerazione D3DXWELDEPSILONSFLAGS</span><span class="sxs-lookup"><span data-stu-id="2324c-103">D3DXWELDEPSILONSFLAGS enumeration</span></span>

<span data-ttu-id="2324c-104">Opzioni per la saldatura dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2324c-104">Options for welding together vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2324c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2324c-105">Syntax</span></span>


```C++
enum _D3DXWELDEPSILONSFLAGS {
  D3DXWELDEPSILONS_WELDALL              = 1, 
  D3DXWELDEPSILONS_WELDPARTIALMATCHES   = 2, 
  D3DXWELDEPSILONS_DONOTREMOVEVERTICES  = 4, 
  D3DXWELDEPSILONS_DONOTSPLIT           = 8 

};
```



## <a name="constants"></a><span data-ttu-id="2324c-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="2324c-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2324c-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**\_WELDALL D3DXWELDEPSILONS**</span><span class="sxs-lookup"><span data-stu-id="2324c-107"><span id="D3DXWELDEPSILONS_WELDALL"></span><span id="d3dxweldepsilons_weldall"></span>**D3DXWELDEPSILONS\_WELDALL**</span></span>
</dt> <dd>

<span data-ttu-id="2324c-108">Unire tutti i vertici presenti nella stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="2324c-108">Weld together all vertices that are at the same location.</span></span> <span data-ttu-id="2324c-109">L'uso di questo flag evita un confronto Epsilon tra i componenti dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2324c-109">Using this flag avoids an epsilon comparison between vertex components.</span></span>

</dd> <dt>

<span data-ttu-id="2324c-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**\_WELDPARTIALMATCHES D3DXWELDEPSILONS**</span><span class="sxs-lookup"><span data-stu-id="2324c-110"><span id="D3DXWELDEPSILONS_WELDPARTIALMATCHES"></span><span id="d3dxweldepsilons_weldpartialmatches"></span>**D3DXWELDEPSILONS\_WELDPARTIALMATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="2324c-111">Se un componente Vertex specificato si trova all'interno di Epsilon, modificare i vertici parzialmente corrispondenti in modo che entrambi i componenti siano identici.</span><span class="sxs-lookup"><span data-stu-id="2324c-111">If a given vertex component is within epsilon, modify partially matched vertices so that both components are identical.</span></span> <span data-ttu-id="2324c-112">Se tutti i componenti sono uguali, rimuovere uno dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2324c-112">If all components are equal, remove one of the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="2324c-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**\_DONOTREMOVEVERTICES D3DXWELDEPSILONS**</span><span class="sxs-lookup"><span data-stu-id="2324c-113"><span id="D3DXWELDEPSILONS_DONOTREMOVEVERTICES"></span><span id="d3dxweldepsilons_donotremovevertices"></span>**D3DXWELDEPSILONS\_DONOTREMOVEVERTICES**</span></span>
</dt> <dd>

<span data-ttu-id="2324c-114">Indica alla saldatura di consentire solo modifiche ai vertici e non alla rimozione.</span><span class="sxs-lookup"><span data-stu-id="2324c-114">Instructs the weld to allow only modifications to vertices and not removal.</span></span> <span data-ttu-id="2324c-115">Questo flag è valido solo se \_ è impostato D3DXWELDEPSILONS WELDPARTIALMATCHES.</span><span class="sxs-lookup"><span data-stu-id="2324c-115">This flag is valid only if D3DXWELDEPSILONS\_WELDPARTIALMATCHES is set.</span></span> <span data-ttu-id="2324c-116">È utile modificare i vertici in modo che siano uguali, ma non consentire la rimozione di vertici.</span><span class="sxs-lookup"><span data-stu-id="2324c-116">It is useful to modify vertices to be equal, but not to allow vertices to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="2324c-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**\_DONOTSPLIT D3DXWELDEPSILONS**</span><span class="sxs-lookup"><span data-stu-id="2324c-117"><span id="D3DXWELDEPSILONS_DONOTSPLIT"></span><span id="d3dxweldepsilons_donotsplit"></span>**D3DXWELDEPSILONS\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="2324c-118">Indica alla saldatura di non suddividere i vertici presenti in gruppi di attributi distinti.</span><span class="sxs-lookup"><span data-stu-id="2324c-118">Instructs the weld not to split vertices that are in separate attribute groups.</span></span> <span data-ttu-id="2324c-119">Quando il metodo [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) viene chiamato con il \_ flag D3DXMESHOPT ATTRSORT, \_ verrà impostato anche il flag D3DXMESHOPT DONOTSPLIT.</span><span class="sxs-lookup"><span data-stu-id="2324c-119">When the [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) method is called with the D3DXMESHOPT\_ATTRSORT flag, then the D3DXMESHOPT\_DONOTSPLIT flag will also be set.</span></span> <span data-ttu-id="2324c-120">L'impostazione di questo flag può rallentare l'elaborazione dei vertici software.</span><span class="sxs-lookup"><span data-stu-id="2324c-120">Setting this flag can slow down software vertex processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2324c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2324c-121">Requirements</span></span>



| <span data-ttu-id="2324c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2324c-122">Requirement</span></span> | <span data-ttu-id="2324c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="2324c-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2324c-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2324c-124">Header</span></span><br/> | <dl> <span data-ttu-id="2324c-125"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="2324c-125"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2324c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2324c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2324c-127">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="2324c-127">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="2324c-128">**D3DXWeldVertices**</span><span class="sxs-lookup"><span data-stu-id="2324c-128">**D3DXWeldVertices**</span></span>](d3dxweldvertices.md)
</dt> </dl>

 

 




