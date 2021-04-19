---
description: Matrice 4x4 che contiene i metodi e gli overload degli operatori.
ms.assetid: c354d28b-bb08-41c5-bb59-90a912181f0f
title: Struttura D3DXMATRIX (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIX
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: cae887e2e9a8782cdc7ba159db203c929006c58a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323417"
---
# <a name="d3dxmatrix-structure-d3dx10mathh"></a><span data-ttu-id="e87c7-103">Struttura D3DXMATRIX (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="e87c7-103">D3DXMATRIX structure (D3DX10Math.h)</span></span>

<span data-ttu-id="e87c7-104">Matrice 4x4 che contiene i metodi e gli overload degli operatori.</span><span class="sxs-lookup"><span data-stu-id="e87c7-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="e87c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e87c7-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="e87c7-106">Members</span><span class="sxs-lookup"><span data-stu-id="e87c7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e87c7-107">**\_IJ**</span><span class="sxs-lookup"><span data-stu-id="e87c7-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="e87c7-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e87c7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e87c7-109">Componente (i, j) della matrice, dove i è il numero di riga e j è il numero di colonna.</span><span class="sxs-lookup"><span data-stu-id="e87c7-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="e87c7-110">34, ad esempio, corrisponde \_ \[ a un ₄ ₃ \] , il componente nella terza riga e nella quarta colonna.</span><span class="sxs-lookup"><span data-stu-id="e87c7-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e87c7-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="e87c7-111">Remarks</span></span>

<span data-ttu-id="e87c7-112">I programmatori C non possono utilizzare la struttura D3DXMATRIX, devono utilizzare la struttura D3DMATRIX.</span><span class="sxs-lookup"><span data-stu-id="e87c7-112">C programmers cannot use the D3DXMATRIX structure, they must use the D3DMATRIX structure.</span></span> <span data-ttu-id="e87c7-113">I programmatori C++ possono sfruttare i costruttori di overload e gli operatori di assegnazione, unario e binari (inclusi uguaglianza).</span><span class="sxs-lookup"><span data-stu-id="e87c7-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="e87c7-114">In D3DX, l' \_ elemento 34 di una matrice di proiezione non può essere un numero negativo.</span><span class="sxs-lookup"><span data-stu-id="e87c7-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="e87c7-115">Se l'applicazione deve usare un valore negativo in questa posizione, deve ridimensionare l'intera matrice di proiezione di-1.</span><span class="sxs-lookup"><span data-stu-id="e87c7-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="e87c7-116">Estensioni D3DXMATRIX</span><span class="sxs-lookup"><span data-stu-id="e87c7-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="e87c7-117">**D3DXMATRIX** include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="e87c7-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


```
#ifdef __cplusplus
typedef struct D3DXMATRIX : public D3DMATRIX
{
public:
    D3DXMATRIX() {};
    D3DXMATRIX( CONST FLOAT * );
    D3DXMATRIX( CONST D3DMATRIX& );
    D3DXMATRIX( CONST D3DXFLOAT16 * );
    D3DXMATRIX( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );


    // access grants
    FLOAT& operator () ( UINT Row, UINT Col );
    FLOAT  operator () ( UINT Row, UINT Col ) const;

    // casting operators
    operator FLOAT* ();
    operator CONST FLOAT* () const;

    // assignment operators
    D3DXMATRIX& operator *= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator += ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator -= ( CONST D3DXMATRIX& );
    D3DXMATRIX& operator *= ( FLOAT );
    D3DXMATRIX& operator /= ( FLOAT );

    // unary operators
    D3DXMATRIX operator + () const;
    D3DXMATRIX operator - () const;

    // binary operators
    D3DXMATRIX operator * ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator + ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator - ( CONST D3DXMATRIX& ) const;
    D3DXMATRIX operator * ( FLOAT ) const;
    D3DXMATRIX operator / ( FLOAT ) const;

    friend D3DXMATRIX operator * ( FLOAT, CONST D3DXMATRIX& );

    BOOL operator == ( CONST D3DXMATRIX& ) const;
    BOOL operator != ( CONST D3DXMATRIX& ) const;

} D3DXMATRIX, *LPD3DXMATRIX;

#else //!__cplusplus
typedef struct _D3DMATRIX D3DXMATRIX, *LPD3DXMATRIX;
#endif //!__cplusplus
        
```



## <a name="requirements"></a><span data-ttu-id="e87c7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e87c7-118">Requirements</span></span>



| <span data-ttu-id="e87c7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e87c7-119">Requirement</span></span> | <span data-ttu-id="e87c7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e87c7-120">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e87c7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e87c7-121">Header</span></span><br/> | <dl> <span data-ttu-id="e87c7-122"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e87c7-122"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e87c7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e87c7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e87c7-124">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="e87c7-124">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
