---
description: Crea un nuovo TAG di elenco per le operazioni di scrittura.
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: SdbBeginWriteListTag (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748746"
---
# <a name="sdbbeginwritelisttag-function"></a><span data-ttu-id="c09d1-103">SdbBeginWriteListTag (funzione)</span><span class="sxs-lookup"><span data-stu-id="c09d1-103">SdbBeginWriteListTag function</span></span>

<span data-ttu-id="c09d1-104">Crea un nuovo TAG di elenco per le operazioni di scrittura.</span><span class="sxs-lookup"><span data-stu-id="c09d1-104">Creates a new list TAG for write operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="c09d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c09d1-105">Syntax</span></span>


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="c09d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c09d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c09d1-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c09d1-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c09d1-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="c09d1-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="c09d1-109">*tTag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c09d1-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c09d1-110">TAG per la nuova voce.</span><span class="sxs-lookup"><span data-stu-id="c09d1-110">The TAG for the new entry.</span></span> <span data-ttu-id="c09d1-111">Questo valore deve essere di tipo **\_ \_ elenco di tipi di tag**.</span><span class="sxs-lookup"><span data-stu-id="c09d1-111">This value must be of type **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c09d1-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c09d1-112">Return value</span></span>

<span data-ttu-id="c09d1-113">La funzione restituisce l' [**TagId**](tagid.md) del nuovo elenco in caso di esito positivo o **TagId \_ null** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="c09d1-113">The function returns the [**TAGID**](tagid.md) of the new list on success or **TAGID\_NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c09d1-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c09d1-114">Requirements</span></span>



| <span data-ttu-id="c09d1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c09d1-115">Requirement</span></span> | <span data-ttu-id="c09d1-116">Valore</span><span class="sxs-lookup"><span data-stu-id="c09d1-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c09d1-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c09d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c09d1-118">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c09d1-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c09d1-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c09d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c09d1-120">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c09d1-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c09d1-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c09d1-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c09d1-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c09d1-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c09d1-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c09d1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c09d1-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="c09d1-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="c09d1-125">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="c09d1-125">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> <dt>

[<span data-ttu-id="c09d1-126">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="c09d1-126">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="c09d1-127">**TAG**</span><span class="sxs-lookup"><span data-stu-id="c09d1-127">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="c09d1-128">Tipi di TAG</span><span class="sxs-lookup"><span data-stu-id="c09d1-128">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="c09d1-129">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="c09d1-129">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




