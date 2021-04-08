---
description: Una matrice con allineamento a 16 byte 4x4 che contiene metodi e overload degli operatori.
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Struttura D3DXMATRIXA16 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMATRIXA16
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: 57d2e5e796b929c87d4724d298758f26088918c4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762005"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a><span data-ttu-id="baabb-103">Struttura D3DXMATRIXA16 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="baabb-103">D3DXMATRIXA16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="baabb-104">Una matrice con allineamento a 16 byte 4x4 che contiene metodi e overload degli operatori.</span><span class="sxs-lookup"><span data-stu-id="baabb-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="baabb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="baabb-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="baabb-106">Members</span><span class="sxs-lookup"><span data-stu-id="baabb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="baabb-107">**\_IJ**</span><span class="sxs-lookup"><span data-stu-id="baabb-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="baabb-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="baabb-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="baabb-109">Componente (i, j) della matrice, dove i è il numero di riga e j è il numero di colonna.</span><span class="sxs-lookup"><span data-stu-id="baabb-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="baabb-110">34, ad esempio, corrisponde \_ \[ a un ₄ ₃ \] , il componente nella terza riga e nella quarta colonna.</span><span class="sxs-lookup"><span data-stu-id="baabb-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="baabb-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="baabb-111">Remarks</span></span>

<span data-ttu-id="baabb-112">Una matrice allineata a 16 byte, quando utilizzata dalle funzioni matematiche D3DX, è stata ottimizzata per migliorare le prestazioni sui processori Intel Pentium 4.</span><span class="sxs-lookup"><span data-stu-id="baabb-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="baabb-113">Le matrici sono allineate indipendentemente dalla posizione in cui vengono create: nello stack di programmi, nell'heap o nell'ambito globale.</span><span class="sxs-lookup"><span data-stu-id="baabb-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="baabb-114">L'allineamento viene eseguito usando \_ \_ declspec (align (16)), che funziona con Visual C++ .NET e con Visual C++ 6,0 solo quando è installato il pacchetto del processore.</span><span class="sxs-lookup"><span data-stu-id="baabb-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="baabb-115">Sfortunatamente, non esiste alcun modo per rilevare il pacchetto del processore, quindi l'allineamento dei byte è attivato per impostazione predefinita solo con Visual C++ .NET.</span><span class="sxs-lookup"><span data-stu-id="baabb-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="baabb-116">I vettori e i quaternioni non sono allineati a byte in D3DX.</span><span class="sxs-lookup"><span data-stu-id="baabb-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="baabb-117">Quando si usano i vettori e i quaternioni con le funzioni matematiche D3DX, usare \_ declspec (align (16)) per generare vettori e quaternioni allineati ai byte, in modo da offrire prestazioni migliori.</span><span class="sxs-lookup"><span data-stu-id="baabb-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="baabb-118">La definizione di \_ declspec è illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="baabb-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="baabb-119">Altri compilatori interpretano D3DXMATRIXA16 come D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="baabb-119">Other compilers interpret D3DXMATRIXA16 as D3DXMATRIX.</span></span> <span data-ttu-id="baabb-120">L'utilizzo di questa struttura in un compilatore che non è effettivamente allineato alla matrice può risultare problematico perché non esporrà bug che ignorano l'allineamento.</span><span class="sxs-lookup"><span data-stu-id="baabb-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="baabb-121">Se, ad esempio, un oggetto D3DXMATRIXA16 si trova all'interno di una struttura o di una classe, è possibile che una [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) venga eseguita con una compressione stretta (ignorando i limiti di 16 byte).</span><span class="sxs-lookup"><span data-stu-id="baabb-121">For example, if a D3DXMATRIXA16 object is inside a structure or class, a [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="baabb-122">Ciò causerebbe interruzioni di compilazione se il compilatore venisse a volte aggiunto allineando la matrice.</span><span class="sxs-lookup"><span data-stu-id="baabb-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16"></a><span data-ttu-id="baabb-123">D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="baabb-123">D3DXMATRIXA16</span></span>

<span data-ttu-id="baabb-124">**D3DXMATRIXA16** include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="baabb-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


```
typedef struct _D3DXMATRIXA16 : public D3DXMATRIX
{
    _D3DXMATRIXA16();
    _D3DXMATRIXA16( CONST FLOAT * f);
    _D3DXMATRIXA16( CONST D3DMATRIX& m);
    _D3DXMATRIXA16( FLOAT _11, FLOAT _12, FLOAT _13, FLOAT _14,
                    FLOAT _21, FLOAT _22, FLOAT _23, FLOAT _24,
                    FLOAT _31, FLOAT _32, FLOAT _33, FLOAT _34,
                    FLOAT _41, FLOAT _42, FLOAT _43, FLOAT _44 );
    void* operator new(size_t s);
    void* operator new[](size_t s);

    // The two operators below are not virtual operators. If you cast
    //   to D3DXMATRIX, do not delete using them
    void operator delete(void* p);
    void operator delete[](void* p);

    struct _D3DXMATRIXA16& operator=(CONST D3DXMATRIX& rhs);
} _D3DXMATRIXA16;

typedef D3DX_ALIGN16 _D3DXMATRIXA16 D3DXMATRIXA16, *LPD3DXMATRIXA16;
        
```



## <a name="requirements"></a><span data-ttu-id="baabb-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="baabb-125">Requirements</span></span>



| <span data-ttu-id="baabb-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="baabb-126">Requirement</span></span> | <span data-ttu-id="baabb-127">Valore</span><span class="sxs-lookup"><span data-stu-id="baabb-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="baabb-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="baabb-128">Header</span></span><br/> | <dl> <span data-ttu-id="baabb-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="baabb-129"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baabb-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="baabb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baabb-131">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="baabb-131">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="baabb-132">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="baabb-132">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> </dl>

 

 
