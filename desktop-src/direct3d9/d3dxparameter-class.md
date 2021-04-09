---
description: Tipo di oggetto.
ms.assetid: ab405984-2ebc-4514-9400-bdb13676eda5
title: Enumerazione D3DXPARAMETER_CLASS (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_CLASS
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: c42bfc9335c38de04ab484193a1e178a122f2210
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886269"
---
# <a name="d3dxparameter_class-enumeration"></a><span data-ttu-id="6269b-103">\_Enumerazione della classe D3DXPARAMETER</span><span class="sxs-lookup"><span data-stu-id="6269b-103">D3DXPARAMETER\_CLASS enumeration</span></span>

<span data-ttu-id="6269b-104">Tipo di oggetto.</span><span class="sxs-lookup"><span data-stu-id="6269b-104">The type of object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6269b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6269b-105">Syntax</span></span>


```C++
typedef enum D3DXPARAMETER_CLASS { 
  D3DXPC_SCALAR,
  D3DXPC_VECTOR,
  D3DXPC_MATRIX_ROWS,
  D3DXPC_MATRIX_COLUMNS,
  D3DXPC_OBJECT,
  D3DXPC_STRUCT,
  D3DXPC_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_CLASS, *LPD3DXPARAMETER_CLASS;
```



## <a name="constants"></a><span data-ttu-id="6269b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="6269b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6269b-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**\_Scalare D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="6269b-107"><span id="D3DXPC_SCALAR"></span><span id="d3dxpc_scalar"></span>**D3DXPC\_SCALAR**</span></span>
</dt> <dd>

<span data-ttu-id="6269b-108">Constant è un valore scalare.</span><span class="sxs-lookup"><span data-stu-id="6269b-108">Constant is a scalar.</span></span>

</dd> <dt>

<span data-ttu-id="6269b-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**\_Vettore D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="6269b-109"><span id="D3DXPC_VECTOR"></span><span id="d3dxpc_vector"></span>**D3DXPC\_VECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="6269b-110">Constant è un vettore.</span><span class="sxs-lookup"><span data-stu-id="6269b-110">Constant is a vector.</span></span>

</dd> <dt>

<span data-ttu-id="6269b-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**\_Righe matrice \_ D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="6269b-111"><span id="D3DXPC_MATRIX_ROWS"></span><span id="d3dxpc_matrix_rows"></span>**D3DXPC\_MATRIX\_ROWS**</span></span>
</dt> <dd>

<span data-ttu-id="6269b-112">Constant è una matrice principale della riga.</span><span class="sxs-lookup"><span data-stu-id="6269b-112">Constant is a row major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6269b-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**\_Colonne della matrice D3DXPC \_**</span><span class="sxs-lookup"><span data-stu-id="6269b-113"><span id="D3DXPC_MATRIX_COLUMNS"></span><span id="d3dxpc_matrix_columns"></span>**D3DXPC\_MATRIX\_COLUMNS**</span></span>
</dt> <dd>

<span data-ttu-id="6269b-114">Constant è una matrice principale della colonna.</span><span class="sxs-lookup"><span data-stu-id="6269b-114">Constant is a column major matrix.</span></span>

</dd> <dt>

<span data-ttu-id="6269b-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**\_Oggetto D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="6269b-115"><span id="D3DXPC_OBJECT"></span><span id="d3dxpc_object"></span>**D3DXPC\_OBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="6269b-116">Constant è una trama, uno shader o una stringa.</span><span class="sxs-lookup"><span data-stu-id="6269b-116">Constant is either a texture, shader, or a string.</span></span>

</dd> <dt>

<span data-ttu-id="6269b-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**\_Struct D3DXPC**</span><span class="sxs-lookup"><span data-stu-id="6269b-117"><span id="D3DXPC_STRUCT"></span><span id="d3dxpc_struct"></span>**D3DXPC\_STRUCT**</span></span>
</dt> <dd>

<span data-ttu-id="6269b-118">Constant è una struttura.</span><span class="sxs-lookup"><span data-stu-id="6269b-118">Constant is a structure.</span></span>

</dd> <dt>

<span data-ttu-id="6269b-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6269b-119"><span id="D3DXPC_FORCE_DWORD"></span><span id="d3dxpc_force_dword"></span>**D3DXPC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="6269b-120">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6269b-120">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="6269b-121">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="6269b-121">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="6269b-122">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="6269b-122">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6269b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6269b-123">Requirements</span></span>



| <span data-ttu-id="6269b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6269b-124">Requirement</span></span> | <span data-ttu-id="6269b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6269b-125">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6269b-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6269b-126">Header</span></span><br/> | <dl> <span data-ttu-id="6269b-127"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6269b-127"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6269b-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6269b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6269b-129">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="6269b-129">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="6269b-130">**\_TYPEINFO D3DXSHADER**</span><span class="sxs-lookup"><span data-stu-id="6269b-130">**D3DXSHADER\_TYPEINFO**</span></span>](d3dxshader-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6269b-131">**D3DXCONSTANT \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="6269b-131">**D3DXCONSTANT\_DESC**</span></span>](d3dxconstant-desc.md)
</dt> </dl>

 

 




