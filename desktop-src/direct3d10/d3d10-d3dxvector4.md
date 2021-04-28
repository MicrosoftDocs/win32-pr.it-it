---
description: "Struttura D3DXVECTOR4 (D3DX10Math.h): descrive un vettore a quattro componenti che include overload dell'operatore e cast di tipi."
ms.assetid: c6348346-f317-48ed-a369-e39fdb4dc1d6
title: Struttura D3DXVECTOR4 (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR4
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 2e3af4c11922d7433c56b9353482eba8d374d5a5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102829"
---
# <a name="d3dxvector4-structure-d3dx10mathh"></a><span data-ttu-id="6e9d6-103">Struttura D3DXVECTOR4 (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="6e9d6-103">D3DXVECTOR4 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="6e9d6-104">Descrive un vettore a quattro componenti che include overload dell'operatore e cast di tipi.</span><span class="sxs-lookup"><span data-stu-id="6e9d6-104">Describes a four-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e9d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e9d6-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
```



## <a name="members"></a><span data-ttu-id="6e9d6-106">Members</span><span class="sxs-lookup"><span data-stu-id="6e9d6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6e9d6-107">**x**</span><span class="sxs-lookup"><span data-stu-id="6e9d6-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="6e9d6-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e9d6-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6e9d6-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="6e9d6-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="6e9d6-110">**y**</span><span class="sxs-lookup"><span data-stu-id="6e9d6-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="6e9d6-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e9d6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6e9d6-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="6e9d6-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="6e9d6-113">**Z**</span><span class="sxs-lookup"><span data-stu-id="6e9d6-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="6e9d6-114">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e9d6-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6e9d6-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="6e9d6-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="6e9d6-116">**w**</span><span class="sxs-lookup"><span data-stu-id="6e9d6-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="6e9d6-117">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6e9d6-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6e9d6-118">Componente w.</span><span class="sxs-lookup"><span data-stu-id="6e9d6-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e9d6-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e9d6-119">Remarks</span></span>

<span data-ttu-id="6e9d6-120">**D3DXVECTOR4** include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="6e9d6-120">**D3DXVECTOR4** has the following C++ extensions.</span></span>

### <a name="d3dxvector4-extensions"></a><span data-ttu-id="6e9d6-121">Estensioni D3DXVECTOR4</span><span class="sxs-lookup"><span data-stu-id="6e9d6-121">D3DXVECTOR4 Extensions</span></span>


```
typedef struct D3DXVECTOR4
{
#ifdef __cplusplus
public:
    D3DXVECTOR4() {};
    D3DXVECTOR4( CONST FLOAT* );
    D3DXVECTOR4( CONST D3DXFLOAT16 * );
    D3DXVECTOR4( CONST D3DVECTOR& xyz, FLOAT w );
    D3DXVECTOR4( FLOAT x, FLOAT y, FLOAT z, FLOAT w );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR4& operator += ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator -= ( CONST D3DXVECTOR4& );
    D3DXVECTOR4& operator *= ( FLOAT );
    D3DXVECTOR4& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR4 operator + () const;
    D3DXVECTOR4 operator - () const;

    // binary operators
    D3DXVECTOR4 operator + ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator - ( CONST D3DXVECTOR4& ) const;
    D3DXVECTOR4 operator * ( FLOAT ) const;
    D3DXVECTOR4 operator / ( FLOAT ) const;

    friend D3DXVECTOR4 operator * ( FLOAT, CONST D3DXVECTOR4& );

    BOOL operator == ( CONST D3DXVECTOR4& ) const;
    BOOL operator != ( CONST D3DXVECTOR4& ) const;

public:
#endif //__cplusplus
    FLOAT x, y, z, w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
        
```



## <a name="requirements"></a><span data-ttu-id="6e9d6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e9d6-122">Requirements</span></span>



| <span data-ttu-id="6e9d6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e9d6-123">Requirement</span></span> | <span data-ttu-id="6e9d6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="6e9d6-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9d6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6e9d6-125">Header</span></span><br/> | <dl> <span data-ttu-id="6e9d6-126"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6e9d6-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e9d6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e9d6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9d6-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="6e9d6-128">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
