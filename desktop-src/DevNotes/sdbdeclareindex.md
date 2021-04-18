---
description: Dichiara un nuovo indice nel database specificato.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: SdbDeclareIndex (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305071"
---
# <a name="sdbdeclareindex-function"></a><span data-ttu-id="08be7-103">SdbDeclareIndex (funzione)</span><span class="sxs-lookup"><span data-stu-id="08be7-103">SdbDeclareIndex function</span></span>

<span data-ttu-id="08be7-104">Dichiara un nuovo indice nel database specificato.</span><span class="sxs-lookup"><span data-stu-id="08be7-104">Declares a new index in the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="08be7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08be7-105">Syntax</span></span>


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a><span data-ttu-id="08be7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="08be7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08be7-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08be7-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08be7-108">Handle per il database shim.</span><span class="sxs-lookup"><span data-stu-id="08be7-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="08be7-109">*tWhich* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08be7-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08be7-110">Questo parametro deve essere **un \_ \_ elenco di tipi di tag**.</span><span class="sxs-lookup"><span data-stu-id="08be7-110">This parameter must be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="08be7-111">*tKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08be7-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08be7-112">TAG che specifica il tipo da utilizzare come chiave.</span><span class="sxs-lookup"><span data-stu-id="08be7-112">The TAG that specifies the type to be used as the key.</span></span> <span data-ttu-id="08be7-113">Questo parametro non può essere un **\_ \_ elenco di tipi di tag**.</span><span class="sxs-lookup"><span data-stu-id="08be7-113">This parameter cannot be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="08be7-114">*dwEntries* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08be7-114">*dwEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08be7-115">Numero di voci da allocare nell'indice.</span><span class="sxs-lookup"><span data-stu-id="08be7-115">The number of entries to allocate in the index.</span></span>

</dd> <dt>

<span data-ttu-id="08be7-116">*bUniqueKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08be7-116">*bUniqueKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08be7-117">Se questo parametro è **true**, l'indice è un indice di chiave univoca.</span><span class="sxs-lookup"><span data-stu-id="08be7-117">If this parameter is **TRUE**, the index is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="08be7-118">*piiIndex* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="08be7-118">*piiIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="08be7-119">**INDEXID** risultante dell'indice appena dichiarato.</span><span class="sxs-lookup"><span data-stu-id="08be7-119">The resulting **INDEXID** of the newly declared index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08be7-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08be7-120">Return value</span></span>

<span data-ttu-id="08be7-121">La funzione restituisce **true** in caso di esito positivo o **false** in caso di errore.</span><span class="sxs-lookup"><span data-stu-id="08be7-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="08be7-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="08be7-122">Remarks</span></span>

<span data-ttu-id="08be7-123">Chiamare questa funzione prima di scrivere tag nel nuovo indice.</span><span class="sxs-lookup"><span data-stu-id="08be7-123">Call this function before writing tags to the new index.</span></span>

## <a name="requirements"></a><span data-ttu-id="08be7-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08be7-124">Requirements</span></span>



| <span data-ttu-id="08be7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="08be7-125">Requirement</span></span> | <span data-ttu-id="08be7-126">Valore</span><span class="sxs-lookup"><span data-stu-id="08be7-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08be7-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08be7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="08be7-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08be7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="08be7-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08be7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="08be7-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="08be7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="08be7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="08be7-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08be7-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08be7-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08be7-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08be7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08be7-134">**INDEXID**</span><span class="sxs-lookup"><span data-stu-id="08be7-134">**INDEXID**</span></span>](indexid.md)
</dt> <dt>

[<span data-ttu-id="08be7-135">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="08be7-135">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="08be7-136">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="08be7-136">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="08be7-137">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="08be7-137">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




