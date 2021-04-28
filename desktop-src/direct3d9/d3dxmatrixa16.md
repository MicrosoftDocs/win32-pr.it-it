---
description: 'Struttura D3DXMATRIXA16 (D3dx9math.h): matrice allineata a 16 byte e 4x4 che contiene metodi e overload degli operatori.'
ms.assetid: c7082fe5-f98b-4ab7-b8c2-7cdbab4848ad
title: Struttura D3DXMATRIXA16 (D3dx9math.h)
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
ms.openlocfilehash: 7bb14f23d041ec2634b9710d5620382d8b93da2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094209"
---
# <a name="d3dxmatrixa16-structure-d3dx9mathh"></a><span data-ttu-id="398df-103">Struttura D3DXMATRIXA16 (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="398df-103">D3DXMATRIXA16 structure (D3dx9math.h)</span></span>

<span data-ttu-id="398df-104">Matrice allineata a 16 byte e 4x4 che contiene metodi e overload dell'operatore.</span><span class="sxs-lookup"><span data-stu-id="398df-104">A 4x4, 16-byte-aligned matrix that contains methods and operator overloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="398df-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="398df-105">Syntax</span></span>


```C++
typedef struct D3DXMATRIXA16 {
  FLOAT _ij;
} D3DXMATRIXA16, *LPD3DXMATRIXA16;
```



## <a name="members"></a><span data-ttu-id="398df-106">Members</span><span class="sxs-lookup"><span data-stu-id="398df-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="398df-107">**\_Ij**</span><span class="sxs-lookup"><span data-stu-id="398df-107">**\_ij**</span></span>
</dt> <dd>

<span data-ttu-id="398df-108">Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="398df-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="398df-109">Componente (i, j) della matrice, dove i è il numero di riga e j è il numero di colonna.</span><span class="sxs-lookup"><span data-stu-id="398df-109">The (i, j) component of the matrix, where i is the row number and j is the column number.</span></span> <span data-ttu-id="398df-110">Ad esempio, \_ 34 indica lo stesso ₃₄ , il componente nella terza riga e nella quarta \[ \] colonna.</span><span class="sxs-lookup"><span data-stu-id="398df-110">For example, \_34 means the same as \[a₃₄\], the component in the third row and fourth column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="398df-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="398df-111">Remarks</span></span>

<span data-ttu-id="398df-112">Una matrice allineata a 16 byte, se usata dalle funzioni matematiche D3DX, è stata ottimizzata per migliorare le prestazioni nei processori Intel Pentium 4.</span><span class="sxs-lookup"><span data-stu-id="398df-112">A 16-byte aligned matrix, when used by D3DX math functions, has been optimized for improved performance on Intel Pentium 4 processors.</span></span> <span data-ttu-id="398df-113">Le matrici sono allineate indipendentemente dalla posizione in cui vengono create: nello stack di programmi, nell'heap o nell'ambito globale.</span><span class="sxs-lookup"><span data-stu-id="398df-113">Matrices are aligned independent of where they are created: on the program stack, in the heap, or in global scope.</span></span> <span data-ttu-id="398df-114">L'allineamento viene ottenuto usando \_ \_ declspec(align(16)), che funziona con Visual C++ .NET e con Visual C++ 6.0 solo quando è installato il pacchetto del processore.</span><span class="sxs-lookup"><span data-stu-id="398df-114">Alignment is accomplished using \_\_declspec(align(16)), which works with Visual C++ .NET and with Visual C++ 6.0 only when the processor pack is installed.</span></span> <span data-ttu-id="398df-115">Sfortunatamente, non è possibile rilevare il pacchetto del processore, quindi l'allineamento dei byte è attivato per impostazione predefinita solo con Visual C++ .NET.</span><span class="sxs-lookup"><span data-stu-id="398df-115">Unfortunately, there is no way to detect the processor pack, so byte alignment is turned on by default only with Visual C++ .NET.</span></span>

<span data-ttu-id="398df-116">I vettori e i quaternioni non sono allineati ai byte in D3DX.</span><span class="sxs-lookup"><span data-stu-id="398df-116">Vectors and quaternions are not byte aligned in D3DX.</span></span> <span data-ttu-id="398df-117">Quando si usano vettori e quaternioni con funzioni matematiche D3DX, usare \_ declspec(align(16)) per generare vettori e quaternioni allineati ai byte, perché le prestazioni saranno notevolmente migliori.</span><span class="sxs-lookup"><span data-stu-id="398df-117">When using vectors and quaternions with D3DX math functions, use \_declspec(align(16)) to generate byte aligned vectors and quaternions, because they will perform significantly better.</span></span> <span data-ttu-id="398df-118">La definizione \_ di declspec è illustrata qui.</span><span class="sxs-lookup"><span data-stu-id="398df-118">The definition of \_declspec is shown here.</span></span>


```
#define D3DX_ALIGN16 __declspec(align(16))
```



<span data-ttu-id="398df-119">Altri compilatori interpretano D3DXMATRIXA16 come D3DXMATRIX.</span><span class="sxs-lookup"><span data-stu-id="398df-119">Other compilers interpret D3DXMATRIXA16 as D3DXMATRIX.</span></span> <span data-ttu-id="398df-120">L'uso di questa struttura in un compilatore che non allinea effettivamente la matrice può risultare problematico perché non espone bug che ignorano l'allineamento.</span><span class="sxs-lookup"><span data-stu-id="398df-120">Using this structure on a compiler that does not actually align the matrix can be problematic because it will not expose bugs that ignore alignment.</span></span> <span data-ttu-id="398df-121">Ad esempio, se un oggetto D3DXMATRIXA16 si trova all'interno di una struttura o di una classe, un [**oggetto memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) potrebbe essere eseguito con un pacchetto stretto (ignorando i limiti di 16 byte).</span><span class="sxs-lookup"><span data-stu-id="398df-121">For example, if a D3DXMATRIXA16 object is inside a structure or class, a [**memcpy**](https://msdn.microsoft.com/library/dswaw1wk(v=VS.71).aspx) might be done with tight packing (ignoring 16-byte boundaries).</span></span> <span data-ttu-id="398df-122">Ciò causerebbe interruzioni di compilazione se il compilatore a volte aggiungesse l'allineamento della matrice.</span><span class="sxs-lookup"><span data-stu-id="398df-122">This would cause build breaks if the compiler were to sometime add matrix aligning.</span></span>

### <a name="d3dxmatrixa16"></a><span data-ttu-id="398df-123">D3DXMATRIXA16</span><span class="sxs-lookup"><span data-stu-id="398df-123">D3DXMATRIXA16</span></span>

<span data-ttu-id="398df-124">**D3DXMATRIXA16** include le estensioni C++ seguenti.</span><span class="sxs-lookup"><span data-stu-id="398df-124">**D3DXMATRIXA16** has the following C++ extensions.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="398df-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="398df-125">Requirements</span></span>



| <span data-ttu-id="398df-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="398df-126">Requirement</span></span> | <span data-ttu-id="398df-127">Valore</span><span class="sxs-lookup"><span data-stu-id="398df-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="398df-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="398df-128">Header</span></span><br/> | <dl> <span data-ttu-id="398df-129"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="398df-129"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="398df-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="398df-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="398df-131">Strutture D3DX</span><span class="sxs-lookup"><span data-stu-id="398df-131">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="398df-132">**D3DXMATRIX**</span><span class="sxs-lookup"><span data-stu-id="398df-132">**D3DXMATRIX**</span></span>](d3dxmatrix.md)
</dt> </dl>

 

 
