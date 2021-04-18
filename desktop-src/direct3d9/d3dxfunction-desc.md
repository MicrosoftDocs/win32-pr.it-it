---
description: Descrive una funzione utilizzata da un effetto.
ms.assetid: 5d9deb82-7fe5-4408-8a6a-b34ecd97e8ba
title: Struttura D3DXFUNCTION_DESC (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFUNCTION_DESC
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: ec53cae4689ebc1795937012259b2e219630568b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322675"
---
# <a name="d3dxfunction_desc-structure"></a><span data-ttu-id="96194-103">\_Struttura D3DXFUNCTION DESC</span><span class="sxs-lookup"><span data-stu-id="96194-103">D3DXFUNCTION\_DESC structure</span></span>

<span data-ttu-id="96194-104">Descrive una funzione utilizzata da un effetto.</span><span class="sxs-lookup"><span data-stu-id="96194-104">Describes a function used by an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="96194-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96194-105">Syntax</span></span>


```C++
typedef struct D3DXFUNCTION_DESC {
  LPCSTR Name;
  UINT   Annotations;
} D3DXFUNCTION_DESC, *LPD3DXFUNCTION_DESC;
```



## <a name="members"></a><span data-ttu-id="96194-106">Members</span><span class="sxs-lookup"><span data-stu-id="96194-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="96194-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="96194-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="96194-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96194-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="96194-109">Nome funzione.</span><span class="sxs-lookup"><span data-stu-id="96194-109">Function name.</span></span>

</dd> <dt>

<span data-ttu-id="96194-110">**annotazioni**</span><span class="sxs-lookup"><span data-stu-id="96194-110">**Annotations**</span></span>
</dt> <dd>

<span data-ttu-id="96194-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="96194-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="96194-112">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="96194-112">Unused.</span></span> <span data-ttu-id="96194-113">Questo membro sarà sempre impostato su zero da [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span><span class="sxs-lookup"><span data-stu-id="96194-113">This member will always be set to zero by [**GetFunctionDesc**](id3dxbaseeffect--getfunctiondesc.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96194-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96194-114">Requirements</span></span>



| <span data-ttu-id="96194-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="96194-115">Requirement</span></span> | <span data-ttu-id="96194-116">Valore</span><span class="sxs-lookup"><span data-stu-id="96194-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="96194-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96194-117">Header</span></span><br/> | <dl> <span data-ttu-id="96194-118"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="96194-118"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96194-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96194-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96194-120">Strutture degli effetti</span><span class="sxs-lookup"><span data-stu-id="96194-120">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> </dl>

 

 
