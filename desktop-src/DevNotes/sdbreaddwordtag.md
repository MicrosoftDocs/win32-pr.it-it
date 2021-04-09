---
Description: Recupera il valore DWORD per il TAGID specificato.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: SdbReadDWORDTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121270"
---
# <a name="sdbreaddwordtag-function"></a><span data-ttu-id="63822-103">SdbReadDWORDTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="63822-103">SdbReadDWORDTag function</span></span>

<span data-ttu-id="63822-104">Recupera il valore **DWORD** per il **TagId** specificato.</span><span class="sxs-lookup"><span data-stu-id="63822-104">Retrieves the **DWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="63822-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63822-105">Syntax</span></span>


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="63822-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63822-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63822-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63822-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63822-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="63822-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="63822-109">*tiWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63822-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63822-110">**TagId** che corrisponde ai dati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="63822-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="63822-111">*dwDefault* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63822-111">*dwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63822-112">Valore predefinito da restituire in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="63822-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63822-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63822-113">Return value</span></span>

<span data-ttu-id="63822-114">La funzione restituisce il valore in caso di esito positivo o *dwDefault* in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="63822-114">The function returns the value on success or *dwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="63822-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63822-115">Requirements</span></span>



| <span data-ttu-id="63822-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="63822-116">Requirement</span></span> | <span data-ttu-id="63822-117">Valore</span><span class="sxs-lookup"><span data-stu-id="63822-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="63822-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63822-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63822-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="63822-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="63822-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63822-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63822-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="63822-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="63822-122">DLL</span><span class="sxs-lookup"><span data-stu-id="63822-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63822-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63822-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63822-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63822-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63822-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="63822-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="63822-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="63822-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="63822-127">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="63822-127">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="63822-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="63822-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




