---
description: Scrive un valore di parola nel database specificato.
ms.assetid: 8f921e14-4a82-4d8e-83fa-beb78118ecb8
title: SdbWriteWORDTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75a5b3eb430901de36d5aca325f928aae266bc39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523314"
---
# <a name="sdbwritewordtag-function"></a><span data-ttu-id="29fef-103">SdbWriteWORDTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="29fef-103">SdbWriteWORDTag function</span></span>

<span data-ttu-id="29fef-104">Scrive un valore di **parola** nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="29fef-104">Writes a **WORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="29fef-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="29fef-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteWORDTag(
  _In_ PDB  pdb,
  _In_ TAG  tTag,
  _In_ WORD wData
);
```



## <a name="parameters"></a><span data-ttu-id="29fef-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="29fef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29fef-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29fef-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29fef-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="29fef-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="29fef-109">*tTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29fef-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29fef-110">TAG per la voce.</span><span class="sxs-lookup"><span data-stu-id="29fef-110">The TAG for the entry.</span></span> <span data-ttu-id="29fef-111">Questo TAG deve essere di tipo **tag \_ \_ Word**.</span><span class="sxs-lookup"><span data-stu-id="29fef-111">This TAG must be of type **TAG\_TYPE\_WORD**.</span></span>

</dd> <dt>

<span data-ttu-id="29fef-112">*wData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29fef-112">*wData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29fef-113">Valore.</span><span class="sxs-lookup"><span data-stu-id="29fef-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29fef-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="29fef-114">Return value</span></span>

<span data-ttu-id="29fef-115">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="29fef-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="29fef-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="29fef-116">Requirements</span></span>



| <span data-ttu-id="29fef-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29fef-117">Requirement</span></span> | <span data-ttu-id="29fef-118">Valore</span><span class="sxs-lookup"><span data-stu-id="29fef-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="29fef-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29fef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29fef-120">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29fef-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="29fef-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="29fef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29fef-122">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29fef-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="29fef-123">DLL</span><span class="sxs-lookup"><span data-stu-id="29fef-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29fef-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29fef-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29fef-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="29fef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29fef-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="29fef-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="29fef-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="29fef-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="29fef-128">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="29fef-128">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="29fef-129">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="29fef-129">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> </dl>

 

 




