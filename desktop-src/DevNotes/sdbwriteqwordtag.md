---
description: Scrive un valore QWORD nel database specificato.
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: SdbWriteQWORDTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58dcaad3487bb1f59a75dd6a671ecb43c9cf1751
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748090"
---
# <a name="sdbwriteqwordtag-function"></a><span data-ttu-id="f4004-103">SdbWriteQWORDTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="f4004-103">SdbWriteQWORDTag function</span></span>

<span data-ttu-id="f4004-104">Scrive un valore **QWORD** nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="f4004-104">Writes a **QWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4004-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4004-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
);
```



## <a name="parameters"></a><span data-ttu-id="f4004-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4004-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4004-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4004-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4004-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="f4004-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="f4004-109">*tTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4004-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4004-110">TAG per la voce.</span><span class="sxs-lookup"><span data-stu-id="f4004-110">The TAG for the entry.</span></span> <span data-ttu-id="f4004-111">Questo TAG deve essere di tipo **tag \_ \_ QWORD**.</span><span class="sxs-lookup"><span data-stu-id="f4004-111">This TAG must be of type **TAG\_TYPE\_QWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="f4004-112">*qwData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4004-112">*qwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4004-113">Valore.</span><span class="sxs-lookup"><span data-stu-id="f4004-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4004-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4004-114">Return value</span></span>

<span data-ttu-id="f4004-115">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="f4004-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4004-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4004-116">Requirements</span></span>



| <span data-ttu-id="f4004-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4004-117">Requirement</span></span> | <span data-ttu-id="f4004-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f4004-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4004-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4004-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f4004-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4004-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f4004-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4004-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f4004-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4004-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f4004-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f4004-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4004-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4004-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4004-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4004-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4004-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="f4004-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="f4004-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="f4004-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="f4004-128">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="f4004-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="f4004-129">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="f4004-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




