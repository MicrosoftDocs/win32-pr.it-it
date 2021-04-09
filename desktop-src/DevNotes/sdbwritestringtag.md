---
description: Scrive una stringa nel database specificato.
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: SdbWriteStringTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ac588d99408d0d7f13bc0fd13d8abe8a6580e69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877530"
---
# <a name="sdbwritestringtag-function"></a><span data-ttu-id="14f0d-103">SdbWriteStringTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="14f0d-103">SdbWriteStringTag function</span></span>

<span data-ttu-id="14f0d-104">Scrive una stringa nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="14f0d-104">Writes a string to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="14f0d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14f0d-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
);
```



## <a name="parameters"></a><span data-ttu-id="14f0d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14f0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14f0d-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14f0d-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f0d-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="14f0d-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="14f0d-109">*tTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14f0d-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f0d-110">TAG per la voce.</span><span class="sxs-lookup"><span data-stu-id="14f0d-110">The TAG for the entry.</span></span> <span data-ttu-id="14f0d-111">Questo TAG deve essere di tipo **tag \_ \_ STRINGREF**.</span><span class="sxs-lookup"><span data-stu-id="14f0d-111">This TAG must be of type **TAG\_TYPE\_STRINGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="14f0d-112">*pwszData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="14f0d-112">*pwszData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14f0d-113">Stringa con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="14f0d-113">The null-terminated string.</span></span> <span data-ttu-id="14f0d-114">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="14f0d-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14f0d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14f0d-115">Return value</span></span>

<span data-ttu-id="14f0d-116">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="14f0d-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="14f0d-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14f0d-117">Requirements</span></span>



| <span data-ttu-id="14f0d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="14f0d-118">Requirement</span></span> | <span data-ttu-id="14f0d-119">Valore</span><span class="sxs-lookup"><span data-stu-id="14f0d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14f0d-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14f0d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="14f0d-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14f0d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="14f0d-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14f0d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="14f0d-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14f0d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="14f0d-124">DLL</span><span class="sxs-lookup"><span data-stu-id="14f0d-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14f0d-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14f0d-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14f0d-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14f0d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14f0d-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="14f0d-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="14f0d-128">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="14f0d-128">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="14f0d-129">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="14f0d-129">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="14f0d-130">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="14f0d-130">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




