---
Description: Recupera il valore QWORD per il TAGID specificato.
ms.assetid: 5fa94a95-c7f3-477b-ab7c-931e8d62d501
title: SdbReadQWORDTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 15227f3d7c3177a226f1b3cc77fc78efd34379d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400894"
---
# <a name="sdbreadqwordtag-function"></a><span data-ttu-id="662d6-103">SdbReadQWORDTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="662d6-103">SdbReadQWORDTag function</span></span>

<span data-ttu-id="662d6-104">Recupera il valore **QWORD** per il **TagId** specificato.</span><span class="sxs-lookup"><span data-stu-id="662d6-104">Retrieves the **QWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="662d6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="662d6-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbReadQWORDTag(
  _In_ PDB       pdb,
  _In_ TAGID     tiWhich,
  _In_ ULONGLONG qwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="662d6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="662d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="662d6-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="662d6-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="662d6-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="662d6-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="662d6-109">*tiWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="662d6-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="662d6-110">**TagId** che corrisponde ai dati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="662d6-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="662d6-111">*qwDefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="662d6-111">*qwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="662d6-112">Valore predefinito da restituire in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="662d6-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="662d6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="662d6-113">Return value</span></span>

<span data-ttu-id="662d6-114">La funzione restituisce il valore in caso di esito positivo o *qwDefault* in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="662d6-114">The function returns the value on success or *qwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="662d6-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="662d6-115">Requirements</span></span>



| <span data-ttu-id="662d6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="662d6-116">Requirement</span></span> | <span data-ttu-id="662d6-117">Valore</span><span class="sxs-lookup"><span data-stu-id="662d6-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="662d6-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="662d6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="662d6-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="662d6-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="662d6-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="662d6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="662d6-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="662d6-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="662d6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="662d6-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="662d6-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="662d6-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="662d6-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="662d6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="662d6-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="662d6-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="662d6-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="662d6-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="662d6-127">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="662d6-127">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="662d6-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="662d6-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




