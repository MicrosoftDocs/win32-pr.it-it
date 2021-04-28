---
description: 'Struttura D3DXVECTOR2 (D3DX10Math.h): descrive un vettore a due componenti che include overload degli operatori e cast di tipo.'
ms.assetid: 5b7b4847-b994-48c6-ae3c-e48ee1716ddd
title: Struttura D3DXVECTOR2 (D3DX10Math.h)
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
ms.openlocfilehash: 972238650fa23e8b7aa435cd91b36f2caf8a4d9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102858"
---
# <a name="d3dxvector2-structure-d3dx10mathh"></a><span data-ttu-id="f650b-103">Struttura D3DXVECTOR2 (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="f650b-103">D3DXVECTOR2 structure (D3DX10Math.h)</span></span>

<span data-ttu-id="f650b-104">Descrive un vettore a due componenti che include gli overload degli operatori e i cast di tipo.</span><span class="sxs-lookup"><span data-stu-id="f650b-104">Describes a two-component vector including operator overloads and type casts.</span></span>

## <a name="syntax"></a><span data-ttu-id="f650b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f650b-105">Syntax</span></span>


```C++
typedef struct D3DXVECTOR2 {
  FLOAT x;
  FLOAT y;
} D3DXVECTOR2, *LPD3DXVECTOR2;
```



## <a name="members"></a><span data-ttu-id="f650b-106">Members</span><span class="sxs-lookup"><span data-stu-id="f650b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f650b-107">**x**</span><span class="sxs-lookup"><span data-stu-id="f650b-107">**x**</span></span>
</dt> <dd>

<span data-ttu-id="f650b-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f650b-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f650b-109">Componente x.</span><span class="sxs-lookup"><span data-stu-id="f650b-109">The x-component.</span></span>

</dd> <dt>

<span data-ttu-id="f650b-110">**y**</span><span class="sxs-lookup"><span data-stu-id="f650b-110">**y**</span></span>
</dt> <dd>

<span data-ttu-id="f650b-111">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f650b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f650b-112">Componente y.</span><span class="sxs-lookup"><span data-stu-id="f650b-112">The y-component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f650b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f650b-113">Remarks</span></span>

<span data-ttu-id="f650b-114">**D3DXVECTOR2** include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="f650b-114">**D3DXVECTOR2** has the following C++ extensions.</span></span>

### <a name="d3dxvector2-extensions"></a><span data-ttu-id="f650b-115">Estensioni D3DXVECTOR2</span><span class="sxs-lookup"><span data-stu-id="f650b-115">D3DXVECTOR2 Extensions</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f650b-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f650b-116">Requirements</span></span>



| <span data-ttu-id="f650b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f650b-117">Requirement</span></span> | <span data-ttu-id="f650b-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f650b-118">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f650b-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f650b-119">Header</span></span><br/> | <dl> <span data-ttu-id="f650b-120"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="f650b-120"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f650b-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f650b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f650b-122">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="f650b-122">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
