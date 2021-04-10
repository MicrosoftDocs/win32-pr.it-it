---
description: Apre il database dettagli AppHelp specificato.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: SdbOpenApphelpDetailsDatabase (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125622"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a><span data-ttu-id="d509d-103">SdbOpenApphelpDetailsDatabase (funzione)</span><span class="sxs-lookup"><span data-stu-id="d509d-103">SdbOpenApphelpDetailsDatabase function</span></span>

<span data-ttu-id="d509d-104">Apre il database dettagli AppHelp specificato.</span><span class="sxs-lookup"><span data-stu-id="d509d-104">Opens the specified Apphelp details database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d509d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d509d-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="d509d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d509d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d509d-107">*pwsDetailsDatabasePath* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="d509d-107">*pwsDetailsDatabasePath* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d509d-108">Percorso del database.</span><span class="sxs-lookup"><span data-stu-id="d509d-108">The database path.</span></span> <span data-ttu-id="d509d-109">Se questo parametro è **null**, viene aperto il database di sistema locale.</span><span class="sxs-lookup"><span data-stu-id="d509d-109">If this parameter is **NULL**, the local system database is opened.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d509d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d509d-110">Return value</span></span>

<span data-ttu-id="d509d-111">La funzione restituisce un handle per il database dettagli apphelp.</span><span class="sxs-lookup"><span data-stu-id="d509d-111">The function returns a handle to the Apphelp details database.</span></span>

## <a name="requirements"></a><span data-ttu-id="d509d-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d509d-112">Requirements</span></span>



| <span data-ttu-id="d509d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="d509d-113">Requirement</span></span> | <span data-ttu-id="d509d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="d509d-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d509d-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d509d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d509d-116">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d509d-116">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d509d-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d509d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d509d-118">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d509d-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d509d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d509d-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d509d-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d509d-120"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




