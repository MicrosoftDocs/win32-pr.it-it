---
description: Recupera i dati binari per il TAGID specificato.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: SdbGetBinaryTagData (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304652"
---
# <a name="sdbgetbinarytagdata-function"></a><span data-ttu-id="beb07-103">SdbGetBinaryTagData (funzione)</span><span class="sxs-lookup"><span data-stu-id="beb07-103">SdbGetBinaryTagData function</span></span>

<span data-ttu-id="beb07-104">Recupera i dati binari per il **TagId** specificato.</span><span class="sxs-lookup"><span data-stu-id="beb07-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb07-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="beb07-105">Syntax</span></span>


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="beb07-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="beb07-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb07-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="beb07-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb07-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="beb07-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="beb07-109">*tiWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="beb07-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb07-110">**TagId** che corrisponde ai dati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="beb07-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb07-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="beb07-111">Return value</span></span>

<span data-ttu-id="beb07-112">La funzione restituisce un puntatore ai dati binari o **null** se **TagId** non è valido.</span><span class="sxs-lookup"><span data-stu-id="beb07-112">The function returns a pointer to the binary data or **NULL** if the **TAGID** is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="beb07-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="beb07-113">Requirements</span></span>



| <span data-ttu-id="beb07-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb07-114">Requirement</span></span> | <span data-ttu-id="beb07-115">Valore</span><span class="sxs-lookup"><span data-stu-id="beb07-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="beb07-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="beb07-116">Minimum supported client</span></span><br/> | <span data-ttu-id="beb07-117">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="beb07-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="beb07-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="beb07-118">Minimum supported server</span></span><br/> | <span data-ttu-id="beb07-119">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="beb07-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="beb07-120">DLL</span><span class="sxs-lookup"><span data-stu-id="beb07-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beb07-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beb07-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb07-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="beb07-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb07-123">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="beb07-123">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="beb07-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="beb07-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="beb07-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="beb07-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="beb07-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="beb07-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




