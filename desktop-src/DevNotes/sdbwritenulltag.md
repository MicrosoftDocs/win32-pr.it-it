---
description: Scrive una voce NULL nel database specificato.
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: SdbWriteNULLTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 662d5c4db31f199df8b3b9f7368aba118ea6e8fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225589"
---
# <a name="sdbwritenulltag-function"></a><span data-ttu-id="e14ee-103">SdbWriteNULLTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="e14ee-103">SdbWriteNULLTag function</span></span>

<span data-ttu-id="e14ee-104">Scrive una voce **null** nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="e14ee-104">Writes a **NULL** entry to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="e14ee-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e14ee-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="e14ee-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e14ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e14ee-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e14ee-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e14ee-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="e14ee-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="e14ee-109">*tTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e14ee-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e14ee-110">TAG per la voce.</span><span class="sxs-lookup"><span data-stu-id="e14ee-110">The TAG for the entry.</span></span> <span data-ttu-id="e14ee-111">Questo TAG deve essere di tipo **tag \_ \_ null**.</span><span class="sxs-lookup"><span data-stu-id="e14ee-111">This TAG must be of type **TAG\_TYPE\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e14ee-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e14ee-112">Return value</span></span>

<span data-ttu-id="e14ee-113">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="e14ee-113">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e14ee-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e14ee-114">Requirements</span></span>



| <span data-ttu-id="e14ee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e14ee-115">Requirement</span></span> | <span data-ttu-id="e14ee-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e14ee-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e14ee-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e14ee-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e14ee-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e14ee-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e14ee-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e14ee-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e14ee-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e14ee-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e14ee-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e14ee-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e14ee-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e14ee-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e14ee-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e14ee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e14ee-124">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="e14ee-124">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="e14ee-125">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e14ee-125">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="e14ee-126">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="e14ee-126">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="e14ee-127">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e14ee-127">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




