---
description: Annulla la registrazione del database specificato, rendendolo non più disponibile.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: SdbUnregisterDatabase (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483117"
---
# <a name="sdbunregisterdatabase-function"></a><span data-ttu-id="c2f48-103">SdbUnregisterDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="c2f48-103">SdbUnregisterDatabase function</span></span>

<span data-ttu-id="c2f48-104">Annulla la registrazione del database specificato, rendendolo non più disponibile.</span><span class="sxs-lookup"><span data-stu-id="c2f48-104">Unregisters the specified database, making it no longer available.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2f48-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2f48-105">Syntax</span></span>


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a><span data-ttu-id="c2f48-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2f48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2f48-107">*pguidDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2f48-107">*pguidDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2f48-108">GUID del database.</span><span class="sxs-lookup"><span data-stu-id="c2f48-108">The GUID of the database.</span></span> <span data-ttu-id="c2f48-109">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="c2f48-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2f48-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2f48-110">Return value</span></span>

<span data-ttu-id="c2f48-111">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="c2f48-111">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2f48-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2f48-112">Requirements</span></span>



| <span data-ttu-id="c2f48-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2f48-113">Requirement</span></span> | <span data-ttu-id="c2f48-114">Valore</span><span class="sxs-lookup"><span data-stu-id="c2f48-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2f48-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2f48-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c2f48-116">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c2f48-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c2f48-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2f48-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c2f48-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c2f48-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c2f48-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c2f48-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2f48-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2f48-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2f48-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2f48-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2f48-122">**SdbRegisterDatabaseEx**</span><span class="sxs-lookup"><span data-stu-id="c2f48-122">**SdbRegisterDatabaseEx**</span></span>](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




