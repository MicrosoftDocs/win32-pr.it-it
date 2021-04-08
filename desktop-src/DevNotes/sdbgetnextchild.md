---
description: Cerca il TAG figlio successivo all'interno dell'elemento padre specificato e restituisce il TAGID dell'elemento figlio successivo.
ms.assetid: c7311f20-15ca-4b2d-a08d-8bb992a3a0cd
title: SdbGetNextChild (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetNextChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f2943eaf0baec84a9473b679743b9eafad3b7fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877693"
---
# <a name="sdbgetnextchild-function"></a><span data-ttu-id="d75ef-103">SdbGetNextChild (funzione)</span><span class="sxs-lookup"><span data-stu-id="d75ef-103">SdbGetNextChild function</span></span>

<span data-ttu-id="d75ef-104">Cerca il TAG figlio successivo all'interno dell'elemento padre specificato e restituisce il **TagId** dell'elemento figlio successivo.</span><span class="sxs-lookup"><span data-stu-id="d75ef-104">Searches for the next child TAG within the specified parent and returns the **TAGID** of the next child.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75ef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d75ef-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetNextChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAGID tiPrev
);
```



## <a name="parameters"></a><span data-ttu-id="d75ef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d75ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75ef-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d75ef-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75ef-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="d75ef-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="d75ef-109">*tiParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d75ef-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75ef-110">**TagId** di inizio della ricerca.</span><span class="sxs-lookup"><span data-stu-id="d75ef-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="d75ef-111">Questo parametro può essere un **\_ \_ elenco di tipi di tag** o **\_ radice TagId** .</span><span class="sxs-lookup"><span data-stu-id="d75ef-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="d75ef-112">*tiPrev* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d75ef-112">*tiPrev* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75ef-113">**TagId** del figlio precedente.</span><span class="sxs-lookup"><span data-stu-id="d75ef-113">The **TAGID** of the previous child.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d75ef-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d75ef-114">Return value</span></span>

<span data-ttu-id="d75ef-115">**TagId** dell'elemento figlio o **TagId \_ null** se non viene trovato alcun elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="d75ef-115">The **TAGID** of the child or **TAGID\_NULL** if no child is found.</span></span>

## <a name="remarks"></a><span data-ttu-id="d75ef-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="d75ef-116">Remarks</span></span>

<span data-ttu-id="d75ef-117">Prima di chiamare questa funzione, chiamare la funzione [**SdbGetFirstChild**](sdbgetfirstchild.md) .</span><span class="sxs-lookup"><span data-stu-id="d75ef-117">Before calling this function, call the [**SdbGetFirstChild**](sdbgetfirstchild.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d75ef-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d75ef-118">Requirements</span></span>



| <span data-ttu-id="d75ef-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="d75ef-119">Requirement</span></span> | <span data-ttu-id="d75ef-120">Valore</span><span class="sxs-lookup"><span data-stu-id="d75ef-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d75ef-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d75ef-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d75ef-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d75ef-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d75ef-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d75ef-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d75ef-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d75ef-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d75ef-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d75ef-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d75ef-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d75ef-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d75ef-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d75ef-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75ef-128">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="d75ef-128">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="d75ef-129">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="d75ef-129">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="d75ef-130">**SdbGetFirstChild**</span><span class="sxs-lookup"><span data-stu-id="d75ef-130">**SdbGetFirstChild**</span></span>](sdbgetfirstchild.md)
</dt> </dl>

 

 




