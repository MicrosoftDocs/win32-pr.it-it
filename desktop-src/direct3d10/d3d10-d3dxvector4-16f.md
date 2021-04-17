---
description: Uguale a D3DXVECTOR4, ma usa valori a virgola mobile a 16 bit per x, y e z.
ms.assetid: 2db5fb3e-ffe0-4bcf-8894-a8bc7eefaf82
title: Struttura D3DXVECTOR4_16F (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: d3d46e6bc5423260e550fd026ca52420b1c392ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354449"
---
# <a name="d3dxvector4_16f-structure"></a><span data-ttu-id="c9a5f-103">\_Struttura D3DXVECTOR4 16F</span><span class="sxs-lookup"><span data-stu-id="c9a5f-103">D3DXVECTOR4\_16F structure</span></span>

<span data-ttu-id="c9a5f-104">Uguale a [**D3DXVECTOR4**](d3d10-d3dxvector4.md), ma usa valori a virgola mobile a 16 bit per x, y e z.</span><span class="sxs-lookup"><span data-stu-id="c9a5f-104">Same as a [**D3DXVECTOR4**](d3d10-d3dxvector4.md), but it uses 16-bit floating point values for x, y, and z.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a5f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9a5f-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4_16F {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="members"></a><span data-ttu-id="c9a5f-106">Members</span><span class="sxs-lookup"><span data-stu-id="c9a5f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9a5f-107">**x**</span><span class="sxs-lookup"><span data-stu-id="c9a5f-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="c9a5f-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a5f-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9a5f-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="c9a5f-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="c9a5f-110">**y**</span><span class="sxs-lookup"><span data-stu-id="c9a5f-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="c9a5f-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a5f-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9a5f-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="c9a5f-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="c9a5f-113">**z**</span><span class="sxs-lookup"><span data-stu-id="c9a5f-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="c9a5f-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a5f-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9a5f-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="c9a5f-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="c9a5f-116">**w**</span><span class="sxs-lookup"><span data-stu-id="c9a5f-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="c9a5f-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9a5f-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9a5f-118">Il componente w.</span><span class="sxs-lookup"><span data-stu-id="c9a5f-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9a5f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c9a5f-119">Remarks</span></span>

<span data-ttu-id="c9a5f-120">**D3DXVECTOR4 \_ 16F** include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9a5f-120">**D3DXVECTOR4\_16F** has the following C++ extensions.</span></span>

### <a name="d3dxvector4_16f-extensions"></a><span data-ttu-id="c9a5f-121">\_Estensioni 16F D3DXVECTOR4</span><span class="sxs-lookup"><span data-stu-id="c9a5f-121">D3DXVECTOR4\_16F Extensions</span></span>


```
typedef struct D3DXVECTOR4_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR4_16F() {};
    D3DXVECTOR4_16F( CONST FLOAT * );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR4_16F( CONST D3DXVECTOR3_16F& xyz, CONST D3DXFLOAT16& w );
    D3DXVECTOR4_16F( CONST D3DXFLOAT16& x, CONST D3DXFLOAT16& y, CONST D3DXFLOAT16& z, CONST D3DXFLOAT16& w );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR4_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR4_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y, z, w;

} D3DXVECTOR4_16F, *LPD3DXVECTOR4_16F;
```



## <a name="requirements"></a><span data-ttu-id="c9a5f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9a5f-122">Requirements</span></span>



| <span data-ttu-id="c9a5f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a5f-123">Requirement</span></span> | <span data-ttu-id="c9a5f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c9a5f-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a5f-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9a5f-125">Header</span></span><br/> | <dl> <span data-ttu-id="c9a5f-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a5f-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9a5f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9a5f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a5f-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="c9a5f-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
