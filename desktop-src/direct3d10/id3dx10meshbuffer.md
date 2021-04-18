---
description: Un buffer mesh è un buffer che contiene i dati relativi a una mesh.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Interfaccia ID3DX10MeshBuffer (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322745"
---
# <a name="id3dx10meshbuffer-interface"></a><span data-ttu-id="6de34-103">Interfaccia ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="6de34-103">ID3DX10MeshBuffer interface</span></span>

<span data-ttu-id="6de34-104">Un buffer mesh è un buffer che contiene i dati relativi a una mesh.</span><span class="sxs-lookup"><span data-stu-id="6de34-104">A mesh buffer is a buffer that contains data about a mesh.</span></span> <span data-ttu-id="6de34-105">Può contenere uno dei cinque tipi diversi di dati, ovvero i dati dei vertici, i dati di indice, i dati adiacenza, i dati degli attributi o i dati del punto rep.</span><span class="sxs-lookup"><span data-stu-id="6de34-105">It can contain one of five different types of data: vertex data, index data, adjacency data, attribute data, or point rep data.</span></span> <span data-ttu-id="6de34-106">La struttura viene usata per accedere a questi cinque tipi di dati tramite le cinque API seguenti: [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh:: GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh:: GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)o [**ID3DX10Mesh:: GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="6de34-106">The structure is used to access these five pieces of data through the following five APIs: [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh::GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md), or [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).</span></span>

## <a name="members"></a><span data-ttu-id="6de34-107">Membri</span><span class="sxs-lookup"><span data-stu-id="6de34-107">Members</span></span>

<span data-ttu-id="6de34-108">L'interfaccia **ID3DX10MeshBuffer** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6de34-108">The **ID3DX10MeshBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6de34-109">**ID3DX10MeshBuffer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="6de34-109">**ID3DX10MeshBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="6de34-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="6de34-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6de34-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="6de34-111">Methods</span></span>

<span data-ttu-id="6de34-112">L'interfaccia **ID3DX10MeshBuffer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="6de34-112">The **ID3DX10MeshBuffer** interface has these methods.</span></span>



| <span data-ttu-id="6de34-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="6de34-113">Method</span></span>                                       | <span data-ttu-id="6de34-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6de34-114">Description</span></span>                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="6de34-115">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="6de34-115">**GetSize**</span></span>](id3dx10meshbuffer-getsize.md) | <span data-ttu-id="6de34-116">Ottiene le dimensioni in byte del buffer mesh.</span><span class="sxs-lookup"><span data-stu-id="6de34-116">Get the size of the mesh buffer, in bytes.</span></span><br/>                      |
| [<span data-ttu-id="6de34-117">**Mappa**</span><span class="sxs-lookup"><span data-stu-id="6de34-117">**Map**</span></span>](id3dx10meshbuffer-map.md)         | <span data-ttu-id="6de34-118">Ottenere un puntatore alla memoria del buffer mesh per modificarne il contenuto.</span><span class="sxs-lookup"><span data-stu-id="6de34-118">Get a pointer to the mesh buffer memory to modify its contents.</span></span><br/> |
| [<span data-ttu-id="6de34-119">**Unmap**</span><span class="sxs-lookup"><span data-stu-id="6de34-119">**Unmap**</span></span>](id3dx10meshbuffer-unmap.md)     | <span data-ttu-id="6de34-120">Annullare un buffer.</span><span class="sxs-lookup"><span data-stu-id="6de34-120">Unmap a buffer.</span></span><br/>                                                 |



 

## <a name="requirements"></a><span data-ttu-id="6de34-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6de34-121">Requirements</span></span>



| <span data-ttu-id="6de34-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6de34-122">Requirement</span></span> | <span data-ttu-id="6de34-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6de34-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6de34-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6de34-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6de34-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6de34-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6de34-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="6de34-126">Library</span></span><br/> | <dl> <span data-ttu-id="6de34-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6de34-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de34-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6de34-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de34-129">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6de34-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
