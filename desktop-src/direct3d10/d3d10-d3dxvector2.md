---
description: Descrive un vettore a due componenti, inclusi gli overload degli operatori e i cast di tipo.
ms.assetid: 5b7b4847-b994-48c6-ae3c-e48ee1716ddd
title: Struttura D3DXVECTOR2 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVECTOR2
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 860c7ddaba61adcd93a38469117b2a95779240a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235122"
---
# <a name="d3dxvector2-structure-d3dx10mathh"></a><span data-ttu-id="3f0b2-103">Struttura D3DXVECTOR2 (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="3f0b2-103">D3DXVECTOR2 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="3f0b2-104">Descrive un vettore a due componenti, inclusi gli overload degli operatori e i cast di tipo.</span><span class="sxs-lookup"><span data-stu-id="3f0b2-104">Describes a two-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f0b2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f0b2-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2 {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
```



## <a name="members"></a><span data-ttu-id="3f0b2-106">Members</span><span class="sxs-lookup"><span data-stu-id="3f0b2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3f0b2-107">**x**</span><span class="sxs-lookup"><span data-stu-id="3f0b2-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="3f0b2-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0b2-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3f0b2-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="3f0b2-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="3f0b2-110">**y**</span><span class="sxs-lookup"><span data-stu-id="3f0b2-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="3f0b2-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0b2-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="3f0b2-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="3f0b2-112">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3f0b2-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="3f0b2-113">Remarks</span></span>

<span data-ttu-id="3f0b2-114">**D3DXVECTOR2** include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="3f0b2-114">**D3DXVECTOR2** has the following C++ extensions.</span></span>

### <a name="d3dxvector2-extensions"></a><span data-ttu-id="3f0b2-115">Estensioni D3DXVECTOR2</span><span class="sxs-lookup"><span data-stu-id="3f0b2-115">D3DXVECTOR2 Extensions</span></span>


```
typedef struct D3DXVECTOR2
{
#ifdef __cplusplus
public:
    D3DXVECTOR2() {};
    D3DXVECTOR2( CONST FLOAT * );
    D3DXVECTOR2( CONST D3DXFLOAT16 * );
    D3DXVECTOR2( FLOAT x, FLOAT y );

    // casting
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXVECTOR2& operator += ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator -= ( CONST D3DXVECTOR2& );
    D3DXVECTOR2& operator *= ( FLOAT );
    D3DXVECTOR2& operator /= ( FLOAT );

    // unary operators
    D3DXVECTOR2 operator + () const;
    D3DXVECTOR2 operator - () const;

    // binary operators
    D3DXVECTOR2 operator + ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator - ( CONST D3DXVECTOR2& ) const;
    D3DXVECTOR2 operator * ( FLOAT ) const;
    D3DXVECTOR2 operator / ( FLOAT ) const;

    friend D3DXVECTOR2 operator * ( FLOAT, CONST D3DXVECTOR2& );

    BOOL operator == ( CONST D3DXVECTOR2& ) const;
    BOOL operator != ( CONST D3DXVECTOR2& ) const;


public:
#endif //__cplusplus
    FLOAT x, y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
        
```



## <a name="requirements"></a><span data-ttu-id="3f0b2-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f0b2-116">Requirements</span></span>



| <span data-ttu-id="3f0b2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f0b2-117">Requirement</span></span> | <span data-ttu-id="3f0b2-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3f0b2-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f0b2-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f0b2-119">Header</span></span><br/> | <dl> <span data-ttu-id="3f0b2-120"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f0b2-120"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f0b2-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f0b2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f0b2-122">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="3f0b2-122">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
