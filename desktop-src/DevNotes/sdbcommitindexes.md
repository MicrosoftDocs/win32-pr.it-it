---
description: Consente di eseguire il commit degli indici appena creati nel database specificato.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: SdbCommitIndexes (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126171"
---
# <a name="sdbcommitindexes-function"></a><span data-ttu-id="a0c5a-103">SdbCommitIndexes (funzione)</span><span class="sxs-lookup"><span data-stu-id="a0c5a-103">SdbCommitIndexes function</span></span>

<span data-ttu-id="a0c5a-104">Consente di eseguire il commit degli indici appena creati nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="a0c5a-104">Commits newly created indexes to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0c5a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a0c5a-105">Syntax</span></span>


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="a0c5a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a0c5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0c5a-107">*PDB* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="a0c5a-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0c5a-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="a0c5a-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0c5a-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a0c5a-109">Return value</span></span>

<span data-ttu-id="a0c5a-110">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="a0c5a-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0c5a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0c5a-111">Requirements</span></span>



| <span data-ttu-id="a0c5a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0c5a-112">Requirement</span></span> | <span data-ttu-id="a0c5a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="a0c5a-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0c5a-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0c5a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a0c5a-115">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a0c5a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a0c5a-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0c5a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a0c5a-117">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0c5a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a0c5a-118">DLL</span><span class="sxs-lookup"><span data-stu-id="a0c5a-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0c5a-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0c5a-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0c5a-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0c5a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0c5a-121">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="a0c5a-121">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="a0c5a-122">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="a0c5a-122">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="a0c5a-123">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="a0c5a-123">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




