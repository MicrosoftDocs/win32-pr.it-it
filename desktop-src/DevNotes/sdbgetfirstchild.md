---
description: Cerca un TAG figlio all'interno dell'elemento padre specificato e restituisce l'TAGID del primo elemento figlio.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: SdbGetFirstChild (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522802"
---
# <a name="sdbgetfirstchild-function"></a><span data-ttu-id="35df2-103">SdbGetFirstChild (funzione)</span><span class="sxs-lookup"><span data-stu-id="35df2-103">SdbGetFirstChild function</span></span>

<span data-ttu-id="35df2-104">Cerca un TAG figlio all'interno dell'elemento padre specificato e restituisce l' **TagId** del primo elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="35df2-104">Searches for a child TAG within the specified parent and returns the **TAGID** of the first child.</span></span>

## <a name="syntax"></a><span data-ttu-id="35df2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="35df2-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a><span data-ttu-id="35df2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="35df2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35df2-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35df2-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35df2-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="35df2-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="35df2-109">*tiParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="35df2-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35df2-110">**TagId** di inizio della ricerca.</span><span class="sxs-lookup"><span data-stu-id="35df2-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="35df2-111">Questo parametro può essere un **\_ \_ elenco di tipi di tag** o **\_ radice TagId** .</span><span class="sxs-lookup"><span data-stu-id="35df2-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35df2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="35df2-112">Return value</span></span>

<span data-ttu-id="35df2-113">**TagId** del primo **\_ valore null** figlio o TagId non è stato trovato alcun elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="35df2-113">The **TAGID** of the first child or **TAGID\_NULL** is no child is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="35df2-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35df2-114">Requirements</span></span>



| <span data-ttu-id="35df2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="35df2-115">Requirement</span></span> | <span data-ttu-id="35df2-116">Valore</span><span class="sxs-lookup"><span data-stu-id="35df2-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35df2-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35df2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="35df2-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="35df2-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="35df2-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35df2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="35df2-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="35df2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="35df2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="35df2-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35df2-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35df2-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35df2-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="35df2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35df2-124">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="35df2-124">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="35df2-125">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="35df2-125">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="35df2-126">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="35df2-126">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
</dt> </dl>

 

 




