---
description: "Struttura D3DXMATRIX (D3dx9math.h): matrice 4x4 che contiene metodi e overload dell'operatore."
ms.assetid: 0911088b-50cf-4c4a-996e-351386fc359b
title: Struttura D3DXMATRIX (D3dx9math.h)
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
- d3dx9math.h
ms.openlocfilehash: fad44c13f7b856270fe6475f9e099f6e1714e064
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094219"
---
# <a name="d3dxmatrix-structure-d3dx9mathh"></a><span data-ttu-id="06fe0-103">Struttura D3DXMATRIX (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="06fe0-103">D3DXMATRIX structure (D3dx9math.h)</span></span>

<span data-ttu-id="06fe0-104">Matrice 4x4 che contiene metodi e overload dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="06fe0-104">A 4x4 matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="06fe0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06fe0-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIX {
  FLOAT _ij;
} D3DXMATRIX, *LPD3DXMATRIX;
```



## <a name="members"></a><span data-ttu-id="06fe0-106">Members</span><span class="sxs-lookup"><span data-stu-id="06fe0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="06fe0-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="06fe0-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="06fe0-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="06fe0-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="06fe0-109">Componente (i, j) della matrice, dove i è il numero di riga e j è il numero di colonna.</span><span class="sxs-lookup"><span data-stu-id="06fe0-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="06fe0-110">Ad esempio, 34 indica lo stesso ₃₄ , il componente \_ nella terza riga e nella quarta \[ \] colonna.</span><span class="sxs-lookup"><span data-stu-id="06fe0-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06fe0-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="06fe0-111">Remarks</span></span>

<span data-ttu-id="06fe0-112">I programmatori C non possono usare la struttura D3DXMATRIX, ma devono usare la [**struttura D3DMATRIX.**](d3dmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="06fe0-112">C programmers cannot use the D3DXMATRIX structure, they must use the [**D3DMATRIX**](d3dmatrix.md) structure.</span></span> <span data-ttu-id="06fe0-113">I programmatori C++ possono sfruttare i costruttori di overload e gli operatori di assegnazione, unari e binari (inclusa l'uguaglianza).</span><span class="sxs-lookup"><span data-stu-id="06fe0-113">C++ programmers can take advantage of overloaded constructors and assignment, unary, and binary (including equality) operators.</span></span>

<span data-ttu-id="06fe0-114">In D3DX \_ l'elemento 34 di una matrice di proiezione non può essere un numero negativo.</span><span class="sxs-lookup"><span data-stu-id="06fe0-114">In D3DX, the \_34 element of a projection matrix cannot be a negative number.</span></span> <span data-ttu-id="06fe0-115">Se l'applicazione deve usare un valore negativo in questa posizione, deve invece ridimensionare l'intera matrice di proiezione di -1.</span><span class="sxs-lookup"><span data-stu-id="06fe0-115">If your application needs to use a negative value in this location, it should scale the entire projection matrix by -1 instead.</span></span>

### <a name="d3dxmatrix-extensions"></a><span data-ttu-id="06fe0-116">Estensioni D3DXMATRIX</span><span class="sxs-lookup"><span data-stu-id="06fe0-116">D3DXMATRIX Extensions</span></span>

<span data-ttu-id="06fe0-117">**D3DXMATRIX** include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="06fe0-117">**D3DXMATRIX** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="06fe0-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06fe0-118">Requirements</span></span>



| <span data-ttu-id="06fe0-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="06fe0-119">Requirement</span></span> | <span data-ttu-id="06fe0-120">Valore</span><span class="sxs-lookup"><span data-stu-id="06fe0-120">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06fe0-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06fe0-121">Header</span></span><br/> | <dl> <span data-ttu-id="06fe0-122"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="06fe0-122"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06fe0-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06fe0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06fe0-124">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="06fe0-124">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="06fe0-125">**D3DMATRIX**</span><span class="sxs-lookup"><span data-stu-id="06fe0-125">**D3DMATRIX**</span></span>](d3dmatrix.md)
</dt> </dl>

 

 
