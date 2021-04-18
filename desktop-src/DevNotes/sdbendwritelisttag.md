---
description: Termina le operazioni di scrittura per l'elenco specificato.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: SdbEndWriteListTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304404"
---
# <a name="sdbendwritelisttag-function"></a><span data-ttu-id="032c1-103">SdbEndWriteListTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="032c1-103">SdbEndWriteListTag function</span></span>

<span data-ttu-id="032c1-104">Termina le operazioni di scrittura per l'elenco specificato.</span><span class="sxs-lookup"><span data-stu-id="032c1-104">Ends the write operations for the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="032c1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="032c1-105">Syntax</span></span>


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a><span data-ttu-id="032c1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="032c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="032c1-107">*PDB* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="032c1-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="032c1-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="032c1-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="032c1-109">*tiList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="032c1-109">*tiList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="032c1-110">[**TagId**](tagid.md) dell'elenco</span><span class="sxs-lookup"><span data-stu-id="032c1-110">The [**TAGID**](tagid.md) of the list</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="032c1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="032c1-111">Return value</span></span>

<span data-ttu-id="032c1-112">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="032c1-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="032c1-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="032c1-113">Remarks</span></span>

<span data-ttu-id="032c1-114">Chiamare questa funzione dopo la scrittura di tutte le voci dell'elenco; verrà contrassegnata la fine dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="032c1-114">Call this function after writing all list entries; it will mark the end of the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="032c1-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="032c1-115">Requirements</span></span>



| <span data-ttu-id="032c1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="032c1-116">Requirement</span></span> | <span data-ttu-id="032c1-117">Valore</span><span class="sxs-lookup"><span data-stu-id="032c1-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="032c1-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="032c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="032c1-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="032c1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="032c1-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="032c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="032c1-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="032c1-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="032c1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="032c1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="032c1-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="032c1-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="032c1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="032c1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="032c1-125">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="032c1-125">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="032c1-126">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="032c1-126">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="032c1-127">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="032c1-127">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




