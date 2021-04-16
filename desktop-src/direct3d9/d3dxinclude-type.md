---
description: Descrive il percorso del file di inclusione.
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: Enumerazione D3DXINCLUDE_TYPE (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 51a4ed41203a9f78ee5fef747f088e9def9033c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530895"
---
# <a name="d3dxinclude_type-enumeration"></a><span data-ttu-id="42ac7-103">\_Enumerazione del tipo D3DXINCLUDE</span><span class="sxs-lookup"><span data-stu-id="42ac7-103">D3DXINCLUDE\_TYPE enumeration</span></span>

<span data-ttu-id="42ac7-104">Descrive il percorso del file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="42ac7-104">Describes the location for the include file.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ac7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42ac7-105">Syntax</span></span>


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="42ac7-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="42ac7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="42ac7-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ locale**</span><span class="sxs-lookup"><span data-stu-id="42ac7-107"><span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="42ac7-108">Cercare il file di inclusione nel progetto locale.</span><span class="sxs-lookup"><span data-stu-id="42ac7-108">Look in the local project for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="42ac7-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**\_Sistema D3DXINC**</span><span class="sxs-lookup"><span data-stu-id="42ac7-109"><span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC\_SYSTEM**</span></span>
</dt> <dd>

<span data-ttu-id="42ac7-110">Esaminare il percorso di sistema per il file di inclusione.</span><span class="sxs-lookup"><span data-stu-id="42ac7-110">Look in the system path for the include file.</span></span>

</dd> <dt>

<span data-ttu-id="42ac7-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="42ac7-111"><span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="42ac7-112">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="42ac7-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="42ac7-113">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="42ac7-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="42ac7-114">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="42ac7-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42ac7-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42ac7-115">Requirements</span></span>



| <span data-ttu-id="42ac7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="42ac7-116">Requirement</span></span> | <span data-ttu-id="42ac7-117">Valore</span><span class="sxs-lookup"><span data-stu-id="42ac7-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ac7-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42ac7-118">Header</span></span><br/> | <dl> <span data-ttu-id="42ac7-119"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="42ac7-119"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ac7-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42ac7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ac7-121">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="42ac7-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




