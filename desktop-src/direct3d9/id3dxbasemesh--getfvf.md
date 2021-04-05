---
description: Ottiene il valore del vertice della funzione fissa.
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: 'Metodo ID3DXBaseMesh:: GetFVF (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7ee76292c30b3dfb0a2e38b060f50ef643ae07ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969394"
---
# <a name="id3dxbasemeshgetfvf-method"></a><span data-ttu-id="9402e-103">Metodo ID3DXBaseMesh:: GetFVF</span><span class="sxs-lookup"><span data-stu-id="9402e-103">ID3DXBaseMesh::GetFVF method</span></span>

<span data-ttu-id="9402e-104">Ottiene il valore del vertice della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="9402e-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9402e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9402e-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="9402e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9402e-106">Parameters</span></span>

<span data-ttu-id="9402e-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="9402e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9402e-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9402e-108">Return value</span></span>

<span data-ttu-id="9402e-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9402e-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9402e-110">Restituisce i codici FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="9402e-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="9402e-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="9402e-111">Remarks</span></span>

<span data-ttu-id="9402e-112">Questo metodo può restituire 0 se non è possibile eseguire il mapping diretto del formato vertex a un codice FVF.</span><span class="sxs-lookup"><span data-stu-id="9402e-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="9402e-113">Ciò si verifica per una mesh creata da una dichiarazione di vertice che non ha lo stesso ordine e gli stessi elementi supportati dai codici FVF.</span><span class="sxs-lookup"><span data-stu-id="9402e-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="9402e-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9402e-114">Requirements</span></span>



| <span data-ttu-id="9402e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9402e-115">Requirement</span></span> | <span data-ttu-id="9402e-116">Valore</span><span class="sxs-lookup"><span data-stu-id="9402e-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9402e-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9402e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9402e-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="9402e-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="9402e-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="9402e-119">Library</span></span><br/> | <dl> <span data-ttu-id="9402e-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9402e-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9402e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9402e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9402e-122">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="9402e-122">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
