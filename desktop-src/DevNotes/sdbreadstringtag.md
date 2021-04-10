---
Description: Recupera la stringa per il TAGID specificato.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: SdbReadStringTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3f368d66e0fbc144a46683a04655cd7f650c3bce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964841"
---
# <a name="sdbreadstringtag-function"></a><span data-ttu-id="61e56-103">SdbReadStringTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="61e56-103">SdbReadStringTag function</span></span>

<span data-ttu-id="61e56-104">Recupera la stringa per il **TagId** specificato.</span><span class="sxs-lookup"><span data-stu-id="61e56-104">Retrieves the string for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="61e56-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61e56-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="61e56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="61e56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61e56-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61e56-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61e56-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="61e56-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="61e56-109">*tiWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61e56-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61e56-110">**TagId** che corrisponde ai dati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="61e56-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="61e56-111">*pwszBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="61e56-111">*pwszBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61e56-112">Buffer che riceve la stringa.</span><span class="sxs-lookup"><span data-stu-id="61e56-112">The buffer that receives the string.</span></span> <span data-ttu-id="61e56-113">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="61e56-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="61e56-114">*cchBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61e56-114">*cchBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61e56-115">Dimensioni del buffer *pwszBuffer* , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="61e56-115">The size of the *pwszBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61e56-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61e56-116">Return value</span></span>

<span data-ttu-id="61e56-117">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="61e56-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="61e56-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61e56-118">Requirements</span></span>



| <span data-ttu-id="61e56-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="61e56-119">Requirement</span></span> | <span data-ttu-id="61e56-120">Valore</span><span class="sxs-lookup"><span data-stu-id="61e56-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61e56-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61e56-121">Minimum supported client</span></span><br/> | <span data-ttu-id="61e56-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="61e56-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="61e56-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="61e56-123">Minimum supported server</span></span><br/> | <span data-ttu-id="61e56-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61e56-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="61e56-125">DLL</span><span class="sxs-lookup"><span data-stu-id="61e56-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61e56-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61e56-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61e56-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61e56-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61e56-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="61e56-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="61e56-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="61e56-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="61e56-130">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="61e56-130">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
</dt> <dt>

[<span data-ttu-id="61e56-131">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="61e56-131">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> </dl>

 

 




