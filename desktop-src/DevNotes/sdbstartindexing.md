---
description: Consente la creazione e la modifica di indici per il database specificato.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: SdbStartIndexing (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e3324b4cb0d42ca33ee7c3234a1acc099adcb743
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126390"
---
# <a name="sdbstartindexing-function"></a><span data-ttu-id="a94b6-103">SdbStartIndexing (funzione)</span><span class="sxs-lookup"><span data-stu-id="a94b6-103">SdbStartIndexing function</span></span>

<span data-ttu-id="a94b6-104">Consente la creazione e la modifica di indici per il database specificato.</span><span class="sxs-lookup"><span data-stu-id="a94b6-104">Enables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a94b6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a94b6-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="a94b6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a94b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a94b6-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a94b6-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a94b6-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="a94b6-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="a94b6-109">*iiWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a94b6-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a94b6-110">Identificatore dell'indice.</span><span class="sxs-lookup"><span data-stu-id="a94b6-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a94b6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a94b6-111">Return value</span></span>

<span data-ttu-id="a94b6-112">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="a94b6-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a94b6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a94b6-113">Requirements</span></span>



| <span data-ttu-id="a94b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a94b6-114">Requirement</span></span> | <span data-ttu-id="a94b6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a94b6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a94b6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a94b6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a94b6-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a94b6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a94b6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a94b6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a94b6-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a94b6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a94b6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a94b6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a94b6-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a94b6-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a94b6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a94b6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a94b6-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="a94b6-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="a94b6-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="a94b6-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="a94b6-125">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="a94b6-125">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




