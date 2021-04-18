---
description: Tipo di dati del registro.
ms.assetid: b54530d3-4267-4b41-9a16-59d400ef3e18
title: Enumerazione D3DXREGISTER_SET (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXREGISTER_SET
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 683b13d0b386fcdbc162293455e2beb11bc1ee85
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322481"
---
# <a name="d3dxregister_set-enumeration"></a><span data-ttu-id="48eb6-103">\_Enumerazione set D3DXREGISTER</span><span class="sxs-lookup"><span data-stu-id="48eb6-103">D3DXREGISTER\_SET enumeration</span></span>

<span data-ttu-id="48eb6-104">Tipo di dati del registro.</span><span class="sxs-lookup"><span data-stu-id="48eb6-104">Data type of the register.</span></span>

## <a name="syntax"></a><span data-ttu-id="48eb6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48eb6-105">Syntax</span></span>


```C++
typedef enum _D3DXREGISTER_SET { 
  D3DXRS_BOOL,
  D3DXRS_INT4,
  D3DXRS_FLOAT4,
  D3DXRS_SAMPLER,
  D3DXRS_FORCE_DWORD  = 0x7fffffff
} D3DXREGISTER_SET, *LPD3DXREGISTER_SET;
```



## <a name="constants"></a><span data-ttu-id="48eb6-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="48eb6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="48eb6-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**\_Bool D3DXRS**</span><span class="sxs-lookup"><span data-stu-id="48eb6-107"><span id="D3DXRS_BOOL"></span><span id="d3dxrs_bool"></span>**D3DXRS\_BOOL**</span></span>
</dt> <dd>

<span data-ttu-id="48eb6-108">.</span><span class="sxs-lookup"><span data-stu-id="48eb6-108">Boolean value.</span></span>

</dd> <dt>

<span data-ttu-id="48eb6-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**\_INT4 D3DXRS**</span><span class="sxs-lookup"><span data-stu-id="48eb6-109"><span id="D3DXRS_INT4"></span><span id="d3dxrs_int4"></span>**D3DXRS\_INT4**</span></span>
</dt> <dd>

<span data-ttu-id="48eb6-110">numero intero 4D.</span><span class="sxs-lookup"><span data-stu-id="48eb6-110">4D integer number.</span></span>

</dd> <dt>

<span data-ttu-id="48eb6-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**\_Float4 D3DXRS**</span><span class="sxs-lookup"><span data-stu-id="48eb6-111"><span id="D3DXRS_FLOAT4"></span><span id="d3dxrs_float4"></span>**D3DXRS\_FLOAT4**</span></span>
</dt> <dd>

<span data-ttu-id="48eb6-112">numero a virgola mobile 4D.</span><span class="sxs-lookup"><span data-stu-id="48eb6-112">4D floating-point number.</span></span>

</dd> <dt>

<span data-ttu-id="48eb6-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**\_Campionatore D3DXRS**</span><span class="sxs-lookup"><span data-stu-id="48eb6-113"><span id="D3DXRS_SAMPLER"></span><span id="d3dxrs_sampler"></span>**D3DXRS\_SAMPLER**</span></span>
</dt> <dd>

<span data-ttu-id="48eb6-114">Il registro contiene i dati del campionatore 4D.</span><span class="sxs-lookup"><span data-stu-id="48eb6-114">The register contains 4D sampler data.</span></span>

</dd> <dt>

<span data-ttu-id="48eb6-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="48eb6-115"><span id="D3DXRS_FORCE_DWORD"></span><span id="d3dxrs_force_dword"></span>**D3DXRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="48eb6-116">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="48eb6-116">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="48eb6-117">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="48eb6-117">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="48eb6-118">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="48eb6-118">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48eb6-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="48eb6-119">Requirements</span></span>



| <span data-ttu-id="48eb6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="48eb6-120">Requirement</span></span> | <span data-ttu-id="48eb6-121">Valore</span><span class="sxs-lookup"><span data-stu-id="48eb6-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48eb6-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="48eb6-122">Header</span></span><br/> | <dl> <span data-ttu-id="48eb6-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="48eb6-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48eb6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48eb6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48eb6-125">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="48eb6-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="48eb6-126">**\_CONSTANTINFO D3DXSHADER**</span><span class="sxs-lookup"><span data-stu-id="48eb6-126">**D3DXSHADER\_CONSTANTINFO**</span></span>](d3dxshader-constantinfo.md)
</dt> <dt>

[<span data-ttu-id="48eb6-127">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="48eb6-127">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




