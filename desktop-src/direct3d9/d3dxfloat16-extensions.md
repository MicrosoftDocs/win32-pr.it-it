---
description: Fornisce gli overload degli operatori e i cast di tipo per le strutture D3DXFLOAT16.
ms.assetid: d287efb5-d15e-46dc-924d-012e1a108efc
title: Estensioni D3DXFLOAT16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFLOAT16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f97e8917f453e7c2c2db99b8f894d557d7b7909f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058604"
---
# <a name="d3dxfloat16-extensions"></a><span data-ttu-id="aa847-103">Estensioni D3DXFLOAT16</span><span class="sxs-lookup"><span data-stu-id="aa847-103">D3DXFLOAT16 Extensions</span></span>

<span data-ttu-id="aa847-104">Fornisce gli overload degli operatori e i cast di tipo per le strutture [**D3DXFLOAT16**](d3dxfloat16.md) .</span><span class="sxs-lookup"><span data-stu-id="aa847-104">Supplies operator overloads and type casts for [**D3DXFLOAT16**](d3dxfloat16.md) structures.</span></span>

``` syntax
typedef struct D3DXFLOAT16
{
#ifdef __cplusplus
public:
    D3DXFLOAT16() {};
    D3DXFLOAT16( FLOAT );
    D3DXFLOAT16( CONST D3DXFLOAT16& );

    // casting
    operator FLOAT ();

    // binary operators
    BOOL operator == ( CONST D3DXFLOAT16& ) const;
    BOOL operator != ( CONST D3DXFLOAT16& ) const;

protected:
#endif //__cplusplus
    WORD value;
} D3DXFLOAT16, *LPD3DXFLOAT16;
```

<span data-ttu-id="aa847-105">Tipi derivati: \* LPD3DXFLOAT16</span><span class="sxs-lookup"><span data-stu-id="aa847-105">Derived types: \*LPD3DXFLOAT16</span></span>

## <a name="members"></a><span data-ttu-id="aa847-106">Membri</span><span class="sxs-lookup"><span data-stu-id="aa847-106">Members</span></span>

<span data-ttu-id="aa847-107">Per ulteriori informazioni sui membri della struttura, fare riferimento a D3DXFLOAT16.</span><span class="sxs-lookup"><span data-stu-id="aa847-107">For more information about structure members, refer to D3DXFLOAT16.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa847-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="aa847-108">Remarks</span></span>

<span data-ttu-id="aa847-109">Gli overload degli operatori e i cast di tipo per questa struttura sono implementati in d3dx9math. inl.</span><span class="sxs-lookup"><span data-stu-id="aa847-109">Operator overloads and type casts for this structure are implemented in d3dx9math.inl.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa847-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aa847-110">Requirements</span></span>



| <span data-ttu-id="aa847-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa847-111">Requirement</span></span> | <span data-ttu-id="aa847-112">Valore</span><span class="sxs-lookup"><span data-stu-id="aa847-112">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa847-113">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aa847-113">Header</span></span><br/> | <dl> <span data-ttu-id="aa847-114"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa847-114"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa847-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aa847-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa847-116">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="aa847-116">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 




