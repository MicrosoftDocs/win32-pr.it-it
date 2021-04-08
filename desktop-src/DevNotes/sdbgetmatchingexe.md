---
description: Cerca il file eseguibile specificato.
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: SdbGetMatchingExe (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877694"
---
# <a name="sdbgetmatchingexe-function"></a><span data-ttu-id="7ff94-103">SdbGetMatchingExe (funzione)</span><span class="sxs-lookup"><span data-stu-id="7ff94-103">SdbGetMatchingExe function</span></span>

<span data-ttu-id="7ff94-104">Cerca il file eseguibile specificato.</span><span class="sxs-lookup"><span data-stu-id="7ff94-104">Searches for the specified executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff94-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ff94-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a><span data-ttu-id="7ff94-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ff94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff94-107">*hSDB* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7ff94-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff94-108">Handle per il database shim restituito dalla funzione [**SdbInitDatabase**](sdbinitdatabase.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff94-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7ff94-109">*szPath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff94-109">*szPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff94-110">Percorso del file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="7ff94-110">The path of the executable.</span></span>

</dd> <dt>

<span data-ttu-id="7ff94-111">*szModuleName* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7ff94-111">*szModuleName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff94-112">Nome del modulo.</span><span class="sxs-lookup"><span data-stu-id="7ff94-112">The module name.</span></span>

</dd> <dt>

<span data-ttu-id="7ff94-113">*pszEnvironment* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="7ff94-113">*pszEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff94-114">Variabili di ambiente da utilizzare come contesto di ricerca.</span><span class="sxs-lookup"><span data-stu-id="7ff94-114">The environment variables to be used as search context.</span></span>

</dd> <dt>

<span data-ttu-id="7ff94-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ff94-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff94-116">Questo parametro può essere 0 o **SDBGMEF \_ Ignora \_ ambiente** (0x1).</span><span class="sxs-lookup"><span data-stu-id="7ff94-116">This parameter can be 0 or **SDBGMEF\_IGNORE\_ENVIRONMENT** (0x1).</span></span>

</dd> <dt>

<span data-ttu-id="7ff94-117">*pQueryResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ff94-117">*pQueryResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ff94-118">Struttura [**SDBQUERYRESULT**](sdbqueryresult.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff94-118">An [**SDBQUERYRESULT**](sdbqueryresult.md) structure.</span></span> <span data-ttu-id="7ff94-119">Se non viene trovata alcuna corrispondenza, la struttura contiene **TAGREF \_ null**.</span><span class="sxs-lookup"><span data-stu-id="7ff94-119">If no match is found, the structure contains **TAGREF\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff94-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ff94-120">Return value</span></span>

<span data-ttu-id="7ff94-121">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="7ff94-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff94-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ff94-122">Remarks</span></span>

<span data-ttu-id="7ff94-123">Una volta completato il [**TAGREF**](tagref.md)restituito, liberarlo utilizzando la funzione [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) .</span><span class="sxs-lookup"><span data-stu-id="7ff94-123">When you have finished with the returned [**TAGREF**](tagref.md), free it using the [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff94-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ff94-124">Requirements</span></span>



| <span data-ttu-id="7ff94-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ff94-125">Requirement</span></span> | <span data-ttu-id="7ff94-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7ff94-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff94-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff94-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff94-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ff94-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7ff94-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff94-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff94-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ff94-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7ff94-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff94-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff94-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff94-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff94-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ff94-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff94-134">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="7ff94-134">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="7ff94-135">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="7ff94-135">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> </dl>

 

 




