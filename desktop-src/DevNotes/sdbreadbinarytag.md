---
Description: Recupera i dati binari per il TAGID specificato.
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: SdbReadBinaryTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 024b432c3210b98721a0cf3058bad0f765287fde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301534"
---
# <a name="sdbreadbinarytag-function"></a><span data-ttu-id="c9ec9-103">SdbReadBinaryTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="c9ec9-103">SdbReadBinaryTag function</span></span>

<span data-ttu-id="c9ec9-104">Recupera i dati binari per il **TagId** specificato.</span><span class="sxs-lookup"><span data-stu-id="c9ec9-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ec9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9ec9-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="c9ec9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9ec9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ec9-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9ec9-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ec9-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="c9ec9-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="c9ec9-109">*tiWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9ec9-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ec9-110">**TagId** che corrisponde ai dati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c9ec9-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c9ec9-111">*pbuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c9ec9-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ec9-112">Buffer che riceve i dati binari.</span><span class="sxs-lookup"><span data-stu-id="c9ec9-112">The buffer that receives the binary data.</span></span> <span data-ttu-id="c9ec9-113">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c9ec9-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c9ec9-114">*dwBufferSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9ec9-114">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ec9-115">Dimensioni in byte del buffer *pbuffer* .</span><span class="sxs-lookup"><span data-stu-id="c9ec9-115">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ec9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9ec9-116">Return value</span></span>

<span data-ttu-id="c9ec9-117">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="c9ec9-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ec9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9ec9-118">Requirements</span></span>



| <span data-ttu-id="c9ec9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9ec9-119">Requirement</span></span> | <span data-ttu-id="c9ec9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c9ec9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ec9-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9ec9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c9ec9-122">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c9ec9-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c9ec9-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9ec9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c9ec9-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c9ec9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c9ec9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c9ec9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9ec9-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9ec9-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9ec9-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9ec9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ec9-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="c9ec9-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="c9ec9-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="c9ec9-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="c9ec9-130">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="c9ec9-130">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="c9ec9-131">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="c9ec9-131">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




