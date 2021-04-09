---
description: Cerca la corrispondenza di TAG successiva all'interno dell'elemento padre specificato e restituisce il TAGID della corrispondenza.
ms.assetid: c96aa1c1-b0e6-49f5-9f74-7d0e050bee3b
title: SdbFindNextTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindNextTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a5baf728a75e4c02c20ed4207b7d6b9a968af1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877537"
---
# <a name="sdbfindnexttag-function"></a><span data-ttu-id="757d3-103">SdbFindNextTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="757d3-103">SdbFindNextTag function</span></span>

<span data-ttu-id="757d3-104">Cerca la corrispondenza di TAG successiva all'interno dell'elemento padre specificato e restituisce il **TagId** della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="757d3-104">Searches for the next TAG match within the specified parent and returns the **TAGID** of the match.</span></span>

## <a name="syntax"></a><span data-ttu-id="757d3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="757d3-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindNextTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="757d3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="757d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="757d3-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="757d3-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="757d3-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="757d3-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="757d3-109">*tiParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="757d3-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="757d3-110">**TagId** di inizio della ricerca.</span><span class="sxs-lookup"><span data-stu-id="757d3-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="757d3-111">Questo parametro può essere un **\_ \_ elenco di tipi di tag** o **\_ radice TagId** .</span><span class="sxs-lookup"><span data-stu-id="757d3-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="757d3-112">*tiPrev* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="757d3-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="757d3-113">**TagId** della corrispondenza precedente.</span><span class="sxs-lookup"><span data-stu-id="757d3-113">The **TAGID** of the previous match.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="757d3-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="757d3-114">Return value</span></span>

<span data-ttu-id="757d3-115">**TagId** della corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="757d3-115">The **TAGID** of the match.</span></span>

## <a name="remarks"></a><span data-ttu-id="757d3-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="757d3-116">Remarks</span></span>

<span data-ttu-id="757d3-117">Prima di chiamare questa funzione, chiamare la funzione [**SdbFindFirstTag**](sdbfindfirsttag.md) .</span><span class="sxs-lookup"><span data-stu-id="757d3-117">Before calling this function, call the [**SdbFindFirstTag**](sdbfindfirsttag.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="757d3-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="757d3-118">Requirements</span></span>



| <span data-ttu-id="757d3-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="757d3-119">Requirement</span></span> | <span data-ttu-id="757d3-120">Valore</span><span class="sxs-lookup"><span data-stu-id="757d3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="757d3-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="757d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="757d3-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="757d3-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="757d3-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="757d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="757d3-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="757d3-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="757d3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="757d3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="757d3-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="757d3-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757d3-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="757d3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757d3-128">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="757d3-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="757d3-129">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="757d3-129">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




