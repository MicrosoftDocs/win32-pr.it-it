---
description: Descrive un vettore a due componenti, inclusi gli overload degli operatori e i cast di tipo. Uguale a D3DXVECTOR2, ma usa valori a virgola mobile a 16 bit per x, y e z.
ms.assetid: b410d2e1-a006-4563-928a-c9000f73c224
title: Struttura D3DXVECTOR2_16F (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2_16F
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 677f4f8c47cdc70791ad98e18582810bbff23920
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103761962"
---
# <a name="d3dxvector2_16f-structure"></a><span data-ttu-id="8ec68-104">\_Struttura D3DXVECTOR2 16F</span><span class="sxs-lookup"><span data-stu-id="8ec68-104">D3DXVECTOR2\_16F structure</span></span>

<span data-ttu-id="8ec68-105">Descrive un vettore a due componenti, inclusi gli overload degli operatori e i cast di tipo.</span><span class="sxs-lookup"><span data-stu-id="8ec68-105">Describes a two-component vector including operator overloads and type casts.</span></span> <span data-ttu-id="8ec68-106">Uguale a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), ma usa valori a virgola mobile a 16 bit per x, y e z.</span><span class="sxs-lookup"><span data-stu-id="8ec68-106">Same as a [**D3DXVECTOR2**](d3d10-d3dxvector2.md), but it uses 16-bit floating point values for x, y, and z.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec68-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8ec68-107">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2_16F {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
```



## <a name="members"></a><span data-ttu-id="8ec68-108">Members</span><span class="sxs-lookup"><span data-stu-id="8ec68-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ec68-109">**x**</span><span class="sxs-lookup"><span data-stu-id="8ec68-109">**x**</span></span>
</dt> <dd>

<span data-ttu-id="8ec68-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ec68-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ec68-111">Componente x.</span><span class="sxs-lookup"><span data-stu-id="8ec68-111">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="8ec68-112">**y**</span><span class="sxs-lookup"><span data-stu-id="8ec68-112">**y**</span></span>
</dt> <dd>

<span data-ttu-id="8ec68-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8ec68-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ec68-114">Componente y.</span><span class="sxs-lookup"><span data-stu-id="8ec68-114">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ec68-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="8ec68-115">Remarks</span></span>

<span data-ttu-id="8ec68-116">**D3DXVECTOR2 \_ 16F** include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="8ec68-116">**D3DXVECTOR2\_16F** has the following C++ extensions.</span></span>

### <a name="d3dxvector2_16f-extensions"></a><span data-ttu-id="8ec68-117">\_Estensioni 16F D3DXVECTOR2</span><span class="sxs-lookup"><span data-stu-id="8ec68-117">D3DXVECTOR2\_16F Extensions</span></span>


```

typedef struct D3DXVECTOR2_16F
{
#ifdef __cplusplus
public:
    D3DXVECTOR2_16F() {};
    D3DXVECTOR2_16F( CONST FLOAT * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 * );
    D3DXVECTOR2_16F( CONST D3DXFLOAT16 &x, CONST D3DXFLOAT16 &y );

    // casting
    operator D3DXFLOAT16* ();
    operator CONST D3DXFLOAT16* () const;

    // binary operators
    BOOL operator == ( CONST D3DXVECTOR2_16F& ) const;
    BOOL operator != ( CONST D3DXVECTOR2_16F& ) const;

public:
#endif //__cplusplus
    D3DXFLOAT16 x, y;

} D3DXVECTOR2_16F, *LPD3DXVECTOR2_16F;
```



## <a name="requirements"></a><span data-ttu-id="8ec68-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8ec68-118">Requirements</span></span>



| <span data-ttu-id="8ec68-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ec68-119">Requirement</span></span> | <span data-ttu-id="8ec68-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8ec68-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec68-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8ec68-121">Header</span></span><br/> | <dl> <span data-ttu-id="8ec68-122"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec68-122"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ec68-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ec68-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec68-124">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="8ec68-124">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
