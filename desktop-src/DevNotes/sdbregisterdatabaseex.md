---
description: Registra il database specificato.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: SdbRegisterDatabaseEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523345"
---
# <a name="sdbregisterdatabaseex-function"></a><span data-ttu-id="d98e6-103">SdbRegisterDatabaseEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="d98e6-103">SdbRegisterDatabaseEx function</span></span>

<span data-ttu-id="d98e6-104">Registra il database specificato.</span><span class="sxs-lookup"><span data-stu-id="d98e6-104">Registers the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98e6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d98e6-105">Syntax</span></span>


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a><span data-ttu-id="d98e6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d98e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d98e6-107">*pszDatabasePath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d98e6-107">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d98e6-108">Percorso del database.</span><span class="sxs-lookup"><span data-stu-id="d98e6-108">The database path.</span></span> <span data-ttu-id="d98e6-109">Questo parametro non può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="d98e6-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d98e6-110">*dwDatabaseType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d98e6-110">*dwDatabaseType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d98e6-111">Tipo di database.</span><span class="sxs-lookup"><span data-stu-id="d98e6-111">The database type.</span></span> <span data-ttu-id="d98e6-112">Vedere [tipi di database shim](shim-database-types.md) per un elenco di valori.</span><span class="sxs-lookup"><span data-stu-id="d98e6-112">See [Shim Database Types](shim-database-types.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="d98e6-113">*pTimeStamp* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="d98e6-113">*pTimeStamp* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d98e6-114">Timestamp del database.</span><span class="sxs-lookup"><span data-stu-id="d98e6-114">The time stamp for the database.</span></span> <span data-ttu-id="d98e6-115">Se questo parametro è **null**, viene utilizzata l'ora di sistema.</span><span class="sxs-lookup"><span data-stu-id="d98e6-115">If this parameter is **NULL**, the system time is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d98e6-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d98e6-116">Return value</span></span>

<span data-ttu-id="d98e6-117">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="d98e6-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="d98e6-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d98e6-118">Remarks</span></span>

<span data-ttu-id="d98e6-119">Prima di poter utilizzare qualsiasi altra funzione SDB, è necessario registrare un database.</span><span class="sxs-lookup"><span data-stu-id="d98e6-119">A database must be registered before you can use any other SDB functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="d98e6-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d98e6-120">Requirements</span></span>



| <span data-ttu-id="d98e6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d98e6-121">Requirement</span></span> | <span data-ttu-id="d98e6-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d98e6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d98e6-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d98e6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d98e6-124">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d98e6-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d98e6-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d98e6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d98e6-126">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d98e6-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d98e6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d98e6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d98e6-128"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d98e6-128"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d98e6-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d98e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98e6-130">**SdbUnregisterDatabase**</span><span class="sxs-lookup"><span data-stu-id="d98e6-130">**SdbUnregisterDatabase**</span></span>](sdbunregisterdatabase.md)
</dt> </dl>

 

 




