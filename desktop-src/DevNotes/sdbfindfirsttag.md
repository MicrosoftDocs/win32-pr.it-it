---
description: Cerca una corrispondenza di TAG all'interno dell'elemento padre specificato e restituisce il TAGID della prima corrispondenza.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: SdbFindFirstTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965873"
---
# <a name="sdbfindfirsttag-function"></a><span data-ttu-id="00743-103">SdbFindFirstTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="00743-103">SdbFindFirstTag function</span></span>

<span data-ttu-id="00743-104">Cerca una corrispondenza di TAG all'interno dell'elemento padre specificato e restituisce il **TagId** della prima corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="00743-104">Searches for a TAG match within the specified parent and returns the **TAGID** of the first match.</span></span>

## <a name="syntax"></a><span data-ttu-id="00743-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="00743-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
);
```



## <a name="parameters"></a><span data-ttu-id="00743-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="00743-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00743-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00743-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00743-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="00743-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="00743-109">*tiParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00743-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00743-110">**TagId** di inizio della ricerca.</span><span class="sxs-lookup"><span data-stu-id="00743-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="00743-111">Questo parametro può essere un **\_ \_ elenco di tipi di tag** o **\_ radice TagId** .</span><span class="sxs-lookup"><span data-stu-id="00743-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="00743-112">*tTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00743-112">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00743-113">TAG per cui trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="00743-113">The TAG to be matched.</span></span> <span data-ttu-id="00743-114">Per un elenco di valori possibili, vedere [tag](tag.md) .</span><span class="sxs-lookup"><span data-stu-id="00743-114">See [TAG](tag.md) for a list of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00743-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="00743-115">Return value</span></span>

<span data-ttu-id="00743-116">**TagId** della prima corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="00743-116">The **TAGID** of the first match.</span></span>

## <a name="requirements"></a><span data-ttu-id="00743-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="00743-117">Requirements</span></span>



| <span data-ttu-id="00743-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="00743-118">Requirement</span></span> | <span data-ttu-id="00743-119">Valore</span><span class="sxs-lookup"><span data-stu-id="00743-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00743-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00743-120">Minimum supported client</span></span><br/> | <span data-ttu-id="00743-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="00743-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="00743-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="00743-122">Minimum supported server</span></span><br/> | <span data-ttu-id="00743-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="00743-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="00743-124">DLL</span><span class="sxs-lookup"><span data-stu-id="00743-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00743-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00743-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00743-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="00743-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00743-127">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="00743-127">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="00743-128">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="00743-128">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




