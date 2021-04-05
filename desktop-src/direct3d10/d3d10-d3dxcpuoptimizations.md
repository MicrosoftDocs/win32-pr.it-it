---
description: Abilita o Disabilita le ottimizzazioni della CPU.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: Funzione D3DXCpuOptimizations (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a0ef276e6d3303acd77c9580b55a9aa49dbe2087
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762202"
---
# <a name="d3dxcpuoptimizations-function"></a><span data-ttu-id="4fbb9-103">D3DXCpuOptimizations (funzione)</span><span class="sxs-lookup"><span data-stu-id="4fbb9-103">D3DXCpuOptimizations function</span></span>

<span data-ttu-id="4fbb9-104">Abilita o Disabilita le ottimizzazioni della CPU.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-104">Enables or disables CPU optimizations.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fbb9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fbb9-105">Syntax</span></span>


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a><span data-ttu-id="4fbb9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fbb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fbb9-107">*Abilita* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fbb9-107">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fbb9-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4fbb9-109">**True** per abilitare le ottimizzazioni della CPU; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-109">**TRUE** to enable CPU optimizations; otherwise **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fbb9-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4fbb9-110">Return value</span></span>

<span data-ttu-id="4fbb9-111">Tipo: **[ **\_ \_ Ottimizzazione CPU D3DX**](d3dx-cpu-optimization.md)**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-111">Type: **[**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)**</span></span>

<span data-ttu-id="4fbb9-112">Restituisce il tipo di CPU rilevato e per il quale sono disponibili le ottimizzazioni (vedere [**D3DX \_ CPU \_ Optimization**](d3dx-cpu-optimization.md)).</span><span class="sxs-lookup"><span data-stu-id="4fbb9-112">Returns the type of CPU detected, and for which optimizations exist (see [**D3DX\_CPU\_OPTIMIZATION**](d3dx-cpu-optimization.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4fbb9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fbb9-113">Requirements</span></span>



| <span data-ttu-id="4fbb9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fbb9-114">Requirement</span></span> | <span data-ttu-id="4fbb9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4fbb9-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4fbb9-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4fbb9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4fbb9-117"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fbb9-117"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="4fbb9-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="4fbb9-118">Library</span></span><br/> | <dl> <span data-ttu-id="4fbb9-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fbb9-119"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4fbb9-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fbb9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fbb9-121">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="4fbb9-121">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
