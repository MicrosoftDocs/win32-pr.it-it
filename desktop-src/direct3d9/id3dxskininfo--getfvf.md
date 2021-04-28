---
description: 'Metodo ID3DXSkinInfo::GetFVF: ottiene il valore del vertice della funzione fissa.'
ms.assetid: 9b80c4b9-2e5b-4965-99b9-ad6c459ef413
title: Metodo ID3DXSkinInfo::GetFVF (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3415f86f778fbb6fb3592927277e399584bc49a9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107159"
---
# <a name="id3dxskininfogetfvf-method"></a><span data-ttu-id="892f8-103">Metodo ID3DXSkinInfo::GetFVF</span><span class="sxs-lookup"><span data-stu-id="892f8-103">ID3DXSkinInfo::GetFVF method</span></span>

<span data-ttu-id="892f8-104">Ottiene il valore del vertice della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="892f8-104">Gets the fixed function vertex value.</span></span>

## <a name="syntax"></a><span data-ttu-id="892f8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="892f8-105">Syntax</span></span>


```C++
DWORD GetFVF();
```



## <a name="parameters"></a><span data-ttu-id="892f8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="892f8-106">Parameters</span></span>

<span data-ttu-id="892f8-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="892f8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="892f8-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="892f8-108">Return value</span></span>

<span data-ttu-id="892f8-109">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="892f8-109">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="892f8-110">Restituisce i codici FVF (Flexible Vertex Format).</span><span class="sxs-lookup"><span data-stu-id="892f8-110">Returns the flexible vertex format (FVF) codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="892f8-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="892f8-111">Remarks</span></span>

<span data-ttu-id="892f8-112">Questo metodo può restituire 0 se il formato del vertice non può essere mappato direttamente a un codice FVF.</span><span class="sxs-lookup"><span data-stu-id="892f8-112">This method can return 0 if the vertex format cannot be mapped directly to an FVF code.</span></span> <span data-ttu-id="892f8-113">Ciò si verifica per una mesh creata da una dichiarazione di vertice che non ha lo stesso ordine e gli elementi supportati dai codici FVF.</span><span class="sxs-lookup"><span data-stu-id="892f8-113">This will occur for a mesh created from a vertex declaration that doesn't have the same order and elements supported by the FVF codes.</span></span>

## <a name="requirements"></a><span data-ttu-id="892f8-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="892f8-114">Requirements</span></span>



| <span data-ttu-id="892f8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="892f8-115">Requirement</span></span> | <span data-ttu-id="892f8-116">Valore</span><span class="sxs-lookup"><span data-stu-id="892f8-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="892f8-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="892f8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="892f8-118"><dt>D3DX9Mesh.h</dt></span><span class="sxs-lookup"><span data-stu-id="892f8-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="892f8-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="892f8-119">Library</span></span><br/> | <dl> <span data-ttu-id="892f8-120"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="892f8-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="892f8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="892f8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="892f8-122">ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="892f8-122">ID3DXSkinInfo</span></span>](id3dxskininfo.md)
</dt> <dt>

[<span data-ttu-id="892f8-123">**ID3DXSkinInfo::SetFVF**</span><span class="sxs-lookup"><span data-stu-id="892f8-123">**ID3DXSkinInfo::SetFVF**</span></span>](id3dxskininfo--setfvf.md)
</dt> </dl>

 

 
