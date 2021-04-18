---
title: Funzione D3D12IsLayoutOpaque (D3dx12. h)
description: Indica se il layout è opaco.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque (funzione)
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322177"
---
# <a name="d3d12islayoutopaque-function"></a><span data-ttu-id="547ed-104">D3D12IsLayoutOpaque (funzione)</span><span class="sxs-lookup"><span data-stu-id="547ed-104">D3D12IsLayoutOpaque function</span></span>

<span data-ttu-id="547ed-105">Indica se il layout è opaco.</span><span class="sxs-lookup"><span data-stu-id="547ed-105">Indicates whether the layout is opaque.</span></span>

## <a name="syntax"></a><span data-ttu-id="547ed-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="547ed-106">Syntax</span></span>


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a><span data-ttu-id="547ed-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="547ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="547ed-108">*Layout*</span><span class="sxs-lookup"><span data-stu-id="547ed-108">*Layout*</span></span> 
</dt> <dd>

<span data-ttu-id="547ed-109">Tipo: **[ **\_ \_ layout trama D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span><span class="sxs-lookup"><span data-stu-id="547ed-109">Type: **[**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**</span></span>

<span data-ttu-id="547ed-110">Layout da controllare come [**\_ \_ layout di trama D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span><span class="sxs-lookup"><span data-stu-id="547ed-110">The layout to check, as a [**D3D12\_TEXTURE\_LAYOUT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="547ed-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="547ed-111">Return value</span></span>

<span data-ttu-id="547ed-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="547ed-112">Type: **bool**</span></span>

<span data-ttu-id="547ed-113">Valore **booleano** che indica se il layout è opaco.</span><span class="sxs-lookup"><span data-stu-id="547ed-113">A **bool** that indicates whether the layout is opaque.</span></span> <span data-ttu-id="547ed-114">Un layout è opaco se il layout di trama D3D12 è sconosciuto o il layout di \_ \_ \_ trama D3D12 64KB non è \_ \_ \_ \_ definito \_ SWIZZLE.</span><span class="sxs-lookup"><span data-stu-id="547ed-114">A layout is opaque if it is D3D12\_TEXTURE\_LAYOUT\_UNKNOWN or D3D12\_TEXTURE\_LAYOUT\_64KB\_UNDEFINED\_SWIZZLE.</span></span>

## <a name="requirements"></a><span data-ttu-id="547ed-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="547ed-115">Requirements</span></span>



| <span data-ttu-id="547ed-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="547ed-116">Requirement</span></span> | <span data-ttu-id="547ed-117">Valore</span><span class="sxs-lookup"><span data-stu-id="547ed-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="547ed-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="547ed-118">Header</span></span><br/>  | <dl> <span data-ttu-id="547ed-119"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="547ed-119"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="547ed-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="547ed-120">Library</span></span><br/> | <dl> <span data-ttu-id="547ed-121"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="547ed-121"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="547ed-122">DLL</span><span class="sxs-lookup"><span data-stu-id="547ed-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="547ed-123"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="547ed-123"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="547ed-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="547ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="547ed-125">Funzioni helper per D3D12</span><span class="sxs-lookup"><span data-stu-id="547ed-125">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





