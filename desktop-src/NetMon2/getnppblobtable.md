---
description: La funzione GetNPPBlobTable recupera una tabella BLOB NPP che rappresenta le schede di rete di registrazione nel computer locale.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: Funzione GetNPPBlobTable (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882910"
---
# <a name="getnppblobtable-function"></a><span data-ttu-id="3704a-103">GetNPPBlobTable (funzione)</span><span class="sxs-lookup"><span data-stu-id="3704a-103">GetNPPBlobTable function</span></span>

<span data-ttu-id="3704a-104">La funzione **GetNPPBlobTable** recupera una tabella BLOB NPP che rappresenta le schede di rete di registrazione nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="3704a-104">The **GetNPPBlobTable** function retrieves an NPP BLOB table that represents the register NICs on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3704a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3704a-105">Syntax</span></span>


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a><span data-ttu-id="3704a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3704a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3704a-107">*hFilterBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3704a-107">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3704a-108">Handle per un BLOB di filtro che limita i BLOB di NPP restituiti nella tabella.</span><span class="sxs-lookup"><span data-stu-id="3704a-108">Handle to a filter BLOB that limits the NPP BLOBs returned in the table.</span></span>

</dd> <dt>

<span data-ttu-id="3704a-109">*ppBlobTable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3704a-109">*ppBlobTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3704a-110">Puntatore a una struttura di [ \_ tabella BLOB](blob-table.md) che contiene almeno un puntatore del BLOB.</span><span class="sxs-lookup"><span data-stu-id="3704a-110">Pointer to a [BLOB\_TABLE](blob-table.md) structure that contains at least one BLOB pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3704a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3704a-111">Return value</span></span>

<span data-ttu-id="3704a-112">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3704a-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3704a-113">Se la funzione ha esito negativo, il valore restituito è uno dei codici di errore seguenti:</span><span class="sxs-lookup"><span data-stu-id="3704a-113">If the function is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="3704a-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3704a-114">Return code</span></span>                                                                                                | <span data-ttu-id="3704a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3704a-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3704a-116"><dt>**NMERR \_ Nessuna \_ \_ dll NPP**</dt></span><span class="sxs-lookup"><span data-stu-id="3704a-116"><dt>**NMERR\_NO\_NPP\_DLL**</dt></span></span> </dl>         | <span data-ttu-id="3704a-117">Non sono state trovate dll nella directory NPP.</span><span class="sxs-lookup"><span data-stu-id="3704a-117">No DLLs were found in the NPP directory.</span></span><br/>                    |
| <dl> <span data-ttu-id="3704a-118"><dt>**NMERR \_ Nessuna \_ \_ dll NPP \_ valida**</dt></span><span class="sxs-lookup"><span data-stu-id="3704a-118"><dt>**NMERR\_NO\_VALID\_NPP\_DLLS**</dt></span></span> </dl> | <span data-ttu-id="3704a-119">Nessuna dll nella directory NPP era una dll NPP valida.</span><span class="sxs-lookup"><span data-stu-id="3704a-119">None of the DLLs in the NPP directory were valid NPP DLLs.</span></span><br/>  |
| <dl> <span data-ttu-id="3704a-120"><dt>**NMERR \_ senza \_ \_ centrali corrispondente**</dt></span><span class="sxs-lookup"><span data-stu-id="3704a-120"><dt>**NMERR\_NO\_MATCHING\_NPPS**</dt></span></span> </dl>   | <span data-ttu-id="3704a-121">I BLOB di NPP sono stati individuati, ma nessuno ha superato il test di filtro.</span><span class="sxs-lookup"><span data-stu-id="3704a-121">NPP BLOBs were discovered, but none passed the filter test.</span></span><br/> |
| <dl> <span data-ttu-id="3704a-122"><dt>**NMERR \_ da \_ \_ memor**</dt></span><span class="sxs-lookup"><span data-stu-id="3704a-122"><dt>**NMERR\_OUT\_OF\_MEMOR**</dt></span></span> </dl>       | <span data-ttu-id="3704a-123">Network Monitor non è stato in grado di allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="3704a-123">Network Monitor was not able to allocate memory.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="3704a-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="3704a-124">Remarks</span></span>

<span data-ttu-id="3704a-125">Il BLOB denominato da *hFilterBlob* può anche essere un BLOB speciale.</span><span class="sxs-lookup"><span data-stu-id="3704a-125">The BLOB named by *hFilterBlob* can also be a special BLOB.</span></span>

<span data-ttu-id="3704a-126">Se si imposta il flag nel BLOB di filtro su **true**, la tabella BLOB restituita può includere anche BLOB speciali.</span><span class="sxs-lookup"><span data-stu-id="3704a-126">If you set the flag in the filter BLOB to **TRUE**, the returned BLOB table can also include special BLOBs .</span></span>

<span data-ttu-id="3704a-127">Se il BLOB denominato da *hFilterBlob* è un BLOB speciale, l'interfaccia utente Network Monitor tenterà di elaborarla.</span><span class="sxs-lookup"><span data-stu-id="3704a-127">If the BLOB named by *hFilterBlob* is a special BLOB, the Network Monitor UI will attempt to process it.</span></span> <span data-ttu-id="3704a-128">Si supponga, ad esempio, che una chiamata precedente restituisca un BLOB speciale dall'oggetto NPP remoto.</span><span class="sxs-lookup"><span data-stu-id="3704a-128">For example, suppose that a previous call returns a special BLOB from the remote NPP.</span></span> <span data-ttu-id="3704a-129">L'applicazione inserisce il tag necessario, il \_ nome del computer.</span><span class="sxs-lookup"><span data-stu-id="3704a-129">The application inserts the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="3704a-130">Il Finder passa quindi questo BLOB all'elemento NPP remoto, che quindi restituisce una tabella dei BLOB di NPP associati al nome del computer.</span><span class="sxs-lookup"><span data-stu-id="3704a-130">The finder then passes this BLOB to the remote NPP, which then returns a table of the NPP BLOBs associated with the machine name.</span></span>

<span data-ttu-id="3704a-131">Per eliminare definitivamente tutti i BLOB restituiti e la tabella BLOB, il chiamante è responsabile della chiamata della funzione **DestroyBlob** .</span><span class="sxs-lookup"><span data-stu-id="3704a-131">To destroy all returned BLOBs and the BLOB table, the caller is responsible for calling the **DestroyBlob** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3704a-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3704a-132">Requirements</span></span>



| <span data-ttu-id="3704a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3704a-133">Requirement</span></span> | <span data-ttu-id="3704a-134">Valore</span><span class="sxs-lookup"><span data-stu-id="3704a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3704a-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3704a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3704a-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3704a-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3704a-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3704a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3704a-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3704a-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3704a-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3704a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="3704a-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3704a-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3704a-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="3704a-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="3704a-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3704a-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3704a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="3704a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3704a-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3704a-144"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




