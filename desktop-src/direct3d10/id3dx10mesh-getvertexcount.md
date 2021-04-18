---
description: Ottenere il numero di vertici nella rete.
ms.assetid: fea8a3b5-ca10-4066-b2ca-6579829d31b6
title: 'Metodo ID3DX10Mesh:: GetVertexCount (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexCount
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 189be6ff6872cfb85c2f336c29dedef2e435382e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323144"
---
# <a name="id3dx10meshgetvertexcount-method"></a><span data-ttu-id="c4eb5-103">Metodo ID3DX10Mesh:: GetVertexCount</span><span class="sxs-lookup"><span data-stu-id="c4eb5-103">ID3DX10Mesh::GetVertexCount method</span></span>

<span data-ttu-id="c4eb5-104">Ottenere il numero di vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="c4eb5-104">Get the number of vertices in the mesh.</span></span> <span data-ttu-id="c4eb5-105">Una mesh può contenere più buffer di vertice (ad esempio, un buffer di vertice può contenere tutti i dati di posizione, un altro può contenere tutti i dati delle coordinate di trama e così via), tuttavia ogni buffer di vertici conterrà lo stesso numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="c4eb5-105">A mesh may contain multiple vertex buffers (i.e. one vertex buffer may contain all position data, another may contains all texture coordinate data, etc.), however each vertex buffer will contain the same number of elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4eb5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4eb5-106">Syntax</span></span>


```C++
UINT GetVertexCount();
```



## <a name="parameters"></a><span data-ttu-id="c4eb5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c4eb5-107">Parameters</span></span>

<span data-ttu-id="c4eb5-108">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c4eb5-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c4eb5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c4eb5-109">Return value</span></span>

<span data-ttu-id="c4eb5-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4eb5-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4eb5-111">Numero di vertici nella rete.</span><span class="sxs-lookup"><span data-stu-id="c4eb5-111">The number of vertices in the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4eb5-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4eb5-112">Requirements</span></span>



| <span data-ttu-id="c4eb5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4eb5-113">Requirement</span></span> | <span data-ttu-id="c4eb5-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c4eb5-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4eb5-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4eb5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="c4eb5-116"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4eb5-116"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4eb5-117">Libreria</span><span class="sxs-lookup"><span data-stu-id="c4eb5-117">Library</span></span><br/> | <dl> <span data-ttu-id="c4eb5-118"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4eb5-118"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4eb5-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c4eb5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4eb5-120">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="c4eb5-120">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="c4eb5-121">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="c4eb5-121">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
