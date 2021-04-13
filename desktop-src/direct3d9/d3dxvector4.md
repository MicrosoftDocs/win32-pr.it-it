---
description: Descrive un vettore a quattro componenti, inclusi gli overload degli operatori e i cast di tipo.
ms.assetid: fbfe7851-7bec-4fa0-b4dc-52f5cb83d0a4
title: Struttura D3DXVECTOR4 (D3dx9math. h)
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
- d3dx9math.h
ms.openlocfilehash: 1647705877d5cacabbaeb79c4055de298e23b68f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104402032"
---
# <a name="d3dxvector4-structure-d3dx9mathh"></a><span data-ttu-id="c8e37-103">Struttura D3DXVECTOR4 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="c8e37-103">D3DXVECTOR4 structure (D3dx9math.h)</span></span>

<span data-ttu-id="c8e37-104">Descrive un vettore a quattro componenti, inclusi gli overload degli operatori e i cast di tipo.</span><span class="sxs-lookup"><span data-stu-id="c8e37-104">Describes a four-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e37-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8e37-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR4 {
  FLOAT x;
  FLOAT y;
  FLOAT z;
  FLOAT w;
} D3DXVECTOR4, *LPD3DXVECTOR4;
```



## <a name="members"></a><span data-ttu-id="c8e37-106">Members</span><span class="sxs-lookup"><span data-stu-id="c8e37-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c8e37-107">**x**</span><span class="sxs-lookup"><span data-stu-id="c8e37-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="c8e37-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8e37-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c8e37-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="c8e37-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="c8e37-110">**y**</span><span class="sxs-lookup"><span data-stu-id="c8e37-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="c8e37-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8e37-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c8e37-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="c8e37-112">The y-component.</span></span>

</dd> <dt>

<span data-ttu-id="c8e37-113">**z**</span><span class="sxs-lookup"><span data-stu-id="c8e37-113">**z**</span></span>
</dt> <dd>

<span data-ttu-id="c8e37-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8e37-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c8e37-115">Componente z.</span><span class="sxs-lookup"><span data-stu-id="c8e37-115">The z-component.</span></span>

</dd> <dt>

<span data-ttu-id="c8e37-116">**w**</span><span class="sxs-lookup"><span data-stu-id="c8e37-116">**w**</span></span>
</dt> <dd>

<span data-ttu-id="c8e37-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c8e37-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c8e37-118">Il componente w.</span><span class="sxs-lookup"><span data-stu-id="c8e37-118">The w-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8e37-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8e37-119">Remarks</span></span>

### <a name="d3dxvector4-extensions"></a><span data-ttu-id="c8e37-120">Estensioni D3DXVECTOR4</span><span class="sxs-lookup"><span data-stu-id="c8e37-120">D3DXVECTOR4 Extensions</span></span>

<span data-ttu-id="c8e37-121">D3DXVECTOR4 include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="c8e37-121">D3DXVECTOR4 has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c8e37-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8e37-122">Requirements</span></span>



| <span data-ttu-id="c8e37-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8e37-123">Requirement</span></span> | <span data-ttu-id="c8e37-124">Valore</span><span class="sxs-lookup"><span data-stu-id="c8e37-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e37-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8e37-125">Header</span></span><br/> | <dl> <span data-ttu-id="c8e37-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8e37-126"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8e37-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8e37-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e37-128">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="c8e37-128">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
