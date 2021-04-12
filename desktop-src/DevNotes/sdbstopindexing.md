---
description: Disabilita la creazione e la modifica di indici per il database specificato.
ms.assetid: d079eae2-574e-4ac1-a0f9-11796e56a790
title: SdbStopIndexing (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStopIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3c9c6b34c265d611b57a3e73bb0c8fb1822fe752
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523329"
---
# <a name="sdbstopindexing-function"></a><span data-ttu-id="5a3b7-103">SdbStopIndexing (funzione)</span><span class="sxs-lookup"><span data-stu-id="5a3b7-103">SdbStopIndexing function</span></span>

<span data-ttu-id="5a3b7-104">Disabilita la creazione e la modifica di indici per il database specificato.</span><span class="sxs-lookup"><span data-stu-id="5a3b7-104">Disables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a3b7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a3b7-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStopIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="5a3b7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5a3b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a3b7-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a3b7-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3b7-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="5a3b7-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="5a3b7-109">*iiWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a3b7-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a3b7-110">Identificatore dell'indice.</span><span class="sxs-lookup"><span data-stu-id="5a3b7-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a3b7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5a3b7-111">Return value</span></span>

<span data-ttu-id="5a3b7-112">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="5a3b7-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a3b7-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5a3b7-113">Requirements</span></span>



| <span data-ttu-id="5a3b7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a3b7-114">Requirement</span></span> | <span data-ttu-id="5a3b7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="5a3b7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a3b7-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a3b7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5a3b7-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5a3b7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5a3b7-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5a3b7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5a3b7-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5a3b7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5a3b7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="5a3b7-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a3b7-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a3b7-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a3b7-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a3b7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a3b7-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="5a3b7-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="5a3b7-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="5a3b7-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="5a3b7-125">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="5a3b7-125">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> </dl>

 

 




