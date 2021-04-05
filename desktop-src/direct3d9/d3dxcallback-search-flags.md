---
description: Flag utilizzati per ottenere informazioni di callback.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: Enumerazione D3DXCALLBACK_SEARCH_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d3302b79734557a5c1f2082ec2a4e95c03790f4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058624"
---
# <a name="d3dxcallback_search_flags-enumeration"></a><span data-ttu-id="f5db8-103">\_Enumerazione flag di ricerca D3DXCALLBACK \_</span><span class="sxs-lookup"><span data-stu-id="f5db8-103">D3DXCALLBACK\_SEARCH\_FLAGS enumeration</span></span>

<span data-ttu-id="f5db8-104">Flag utilizzati per ottenere informazioni di callback.</span><span class="sxs-lookup"><span data-stu-id="f5db8-104">Flags used to obtain callback information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5db8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5db8-105">Syntax</span></span>


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="f5db8-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="f5db8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f5db8-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**\_Ricerca D3DXCALLBACK \_ esclusa la \_ \_ posizione iniziale**</span><span class="sxs-lookup"><span data-stu-id="f5db8-107"><span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK\_SEARCH\_EXCLUDING\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="f5db8-108">Escludere i callback che si trovano nella posizione iniziale dalla ricerca.</span><span class="sxs-lookup"><span data-stu-id="f5db8-108">Exclude callbacks located at the initial position from the search.</span></span>

</dd> <dt>

<span data-ttu-id="f5db8-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**\_Ricerca D3DXCALLBACK \_ dietro \_ la \_ posizione iniziale**</span><span class="sxs-lookup"><span data-stu-id="f5db8-109"><span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK\_SEARCH\_BEHIND\_INITIAL\_POSITION**</span></span>
</dt> <dd>

<span data-ttu-id="f5db8-110">Invertire la direzione della ricerca di callback.</span><span class="sxs-lookup"><span data-stu-id="f5db8-110">Reverse the callback search direction.</span></span>

</dd> <dt>

<span data-ttu-id="f5db8-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK \_ Search \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f5db8-111"><span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK\_SEARCH\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f5db8-112">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f5db8-112">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f5db8-113">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="f5db8-113">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f5db8-114">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="f5db8-114">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5db8-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5db8-115">Requirements</span></span>



| <span data-ttu-id="f5db8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5db8-116">Requirement</span></span> | <span data-ttu-id="f5db8-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f5db8-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5db8-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5db8-118">Header</span></span><br/> | <dl> <span data-ttu-id="f5db8-119"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5db8-119"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5db8-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5db8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5db8-121">Enumerazioni D3DX</span><span class="sxs-lookup"><span data-stu-id="f5db8-121">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




