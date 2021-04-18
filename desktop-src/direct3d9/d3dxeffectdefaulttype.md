---
description: Tipi di dati effettivi. I dati sono contenuti nel membro pValue di D3DXEFFECTDEFAULT.
ms.assetid: d698ad6e-2ce2-48d6-90be-49bc08f172a9
title: Enumerazione D3DXEFFECTDEFAULTTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXEFFECTDEFAULTTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: ffd31167d712a8270011c061cd6328aa9214352e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322708"
---
# <a name="d3dxeffectdefaulttype-enumeration"></a><span data-ttu-id="0044e-104">Enumerazione D3DXEFFECTDEFAULTTYPE</span><span class="sxs-lookup"><span data-stu-id="0044e-104">D3DXEFFECTDEFAULTTYPE enumeration</span></span>

<span data-ttu-id="0044e-105">Tipi di dati effettivi.</span><span class="sxs-lookup"><span data-stu-id="0044e-105">Effect data types.</span></span> <span data-ttu-id="0044e-106">I dati sono contenuti nel membro pValue di [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span><span class="sxs-lookup"><span data-stu-id="0044e-106">The data is contained in the pValue member of [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0044e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0044e-107">Syntax</span></span>


```C++
typedef enum D3DXEFFECTDEFAULTTYPE { 
  D3DXEDT_STRING      = 1,
  D3DXEDT_FLOATS      = 2,
  D3DXEDT_DWORD       = 3,
  D3DXEDT_FORCEDWORD  = 0x7fffffff
} D3DXEFFECTDEFAULTTYPE, *LPD3DXEFFECTDEFAULTTYPE;
```



## <a name="constants"></a><span data-ttu-id="0044e-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="0044e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0044e-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**\_Stringa D3DXEDT**</span><span class="sxs-lookup"><span data-stu-id="0044e-109"><span id="D3DXEDT_STRING"></span><span id="d3dxedt_string"></span>**D3DXEDT\_STRING**</span></span>
</dt> <dd>

<span data-ttu-id="0044e-110">Il tipo di dati è una stringa di testo ASCII con terminazione NULL.</span><span class="sxs-lookup"><span data-stu-id="0044e-110">The data type is a NULL-terminated ASCII text string.</span></span>

</dd> <dt>

<span data-ttu-id="0044e-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**\_Float D3DXEDT**</span><span class="sxs-lookup"><span data-stu-id="0044e-111"><span id="D3DXEDT_FLOATS"></span><span id="d3dxedt_floats"></span>**D3DXEDT\_FLOATS**</span></span>
</dt> <dd>

<span data-ttu-id="0044e-112">Il tipo di dati è una matrice di tipo float.</span><span class="sxs-lookup"><span data-stu-id="0044e-112">The data type is an array of type float.</span></span> <span data-ttu-id="0044e-113">Il numero di tipi float nella matrice è specificato da NumBytes in [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span><span class="sxs-lookup"><span data-stu-id="0044e-113">The number of float types in the array is specified by NumBytes in [**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md).</span></span>

</dd> <dt>

<span data-ttu-id="0044e-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**\_DWORD D3DXEDT**</span><span class="sxs-lookup"><span data-stu-id="0044e-114"><span id="D3DXEDT_DWORD"></span><span id="d3dxedt_dword"></span>**D3DXEDT\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0044e-115">Il tipo di dati è un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="0044e-115">The data type is a DWORD.</span></span>

</dd> <dt>

<span data-ttu-id="0044e-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**\_FORCEDWORD D3DXEDT**</span><span class="sxs-lookup"><span data-stu-id="0044e-116"><span id="D3DXEDT_FORCEDWORD"></span><span id="d3dxedt_forcedword"></span>**D3DXEDT\_FORCEDWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0044e-117">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0044e-117">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0044e-118">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="0044e-118">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0044e-119">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="0044e-119">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0044e-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0044e-120">Requirements</span></span>



| <span data-ttu-id="0044e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0044e-121">Requirement</span></span> | <span data-ttu-id="0044e-122">Valore</span><span class="sxs-lookup"><span data-stu-id="0044e-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0044e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0044e-123">Header</span></span><br/> | <dl> <span data-ttu-id="0044e-124"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="0044e-124"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0044e-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0044e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0044e-126">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="0044e-126">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




