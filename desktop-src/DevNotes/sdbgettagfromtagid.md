---
description: Recupera il TAG associato all'oggetto TAGID specificato.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: SdbGetTagFromTagID (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126723"
---
# <a name="sdbgettagfromtagid-function"></a><span data-ttu-id="6b2b9-103">SdbGetTagFromTagID (funzione)</span><span class="sxs-lookup"><span data-stu-id="6b2b9-103">SdbGetTagFromTagID function</span></span>

<span data-ttu-id="6b2b9-104">Recupera il TAG associato all'oggetto **TagId** specificato.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-104">Retrieves the TAG associated with the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b2b9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b2b9-105">Syntax</span></span>


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="6b2b9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b2b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b2b9-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b2b9-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b2b9-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="6b2b9-109">*tiWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6b2b9-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b2b9-110">**TagId** per il tag.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-110">The **TAGID** for the TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b2b9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b2b9-111">Return value</span></span>

<span data-ttu-id="6b2b9-112">La funzione restituisce il TAG.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-112">The function returns the TAG.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b2b9-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b2b9-113">Requirements</span></span>



| <span data-ttu-id="6b2b9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b2b9-114">Requirement</span></span> | <span data-ttu-id="6b2b9-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6b2b9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2b9-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b2b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b2b9-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6b2b9-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6b2b9-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b2b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b2b9-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6b2b9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6b2b9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6b2b9-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b2b9-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b2b9-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b2b9-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b2b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b2b9-123">**TAG**</span><span class="sxs-lookup"><span data-stu-id="6b2b9-123">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="6b2b9-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="6b2b9-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




