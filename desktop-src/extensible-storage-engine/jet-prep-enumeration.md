---
description: 'Altre informazioni su: Enumerazione JET_prep'
title: Enumerazione JET_prep
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316478"
---
# <a name="jet_prep-enumeration"></a><span data-ttu-id="b8e2a-103">Enumerazione JET_prep</span><span class="sxs-lookup"><span data-stu-id="b8e2a-103">JET_prep enumeration</span></span>

<span data-ttu-id="b8e2a-104">Tipi di aggiornamento per JetPrepareUpdate.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-104">Update types for JetPrepareUpdate.</span></span>

<span data-ttu-id="b8e2a-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8e2a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8e2a-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8e2a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e2a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8e2a-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a><span data-ttu-id="b8e2a-108">Members</span><span class="sxs-lookup"><span data-stu-id="b8e2a-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="b8e2a-109">Nome del membro</span><span class="sxs-lookup"><span data-stu-id="b8e2a-109">Member name</span></span></th>
<th><span data-ttu-id="b8e2a-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8e2a-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b8e2a-111">Insert</span><span class="sxs-lookup"><span data-stu-id="b8e2a-111">Insert</span></span></td>
<td><span data-ttu-id="b8e2a-112">Questo flag determina la preparazione del cursore per l'inserimento di un nuovo record.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-112">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="b8e2a-113">Tutti i dati vengono inizializzati sullo stato predefinito per il record.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-113">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="b8e2a-114">Se la tabella include una colonna con incremento automatico, a questo record viene assegnato un nuovo valore indipendentemente dal fatto che l'aggiornamento abbia esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-114">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b8e2a-115">Sostituisci</span><span class="sxs-lookup"><span data-stu-id="b8e2a-115">Replace</span></span></td>
<td><span data-ttu-id="b8e2a-116">Questo flag determina la preparazione del cursore per la sostituzione del record corrente.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-116">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="b8e2a-117">Se la tabella contiene una colonna versione, la colonna Version viene impostata sul valore successivo nella sequenza.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-117">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="b8e2a-118">Se l'aggiornamento non viene completato, il valore della versione nel record non sarà interessato.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-118">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="b8e2a-119">Viene assunto un blocco di aggiornamento sul record per impedire ad altre sessioni di aggiornare questo record prima del completamento della sessione.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-119">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b8e2a-120">Annulla</span><span class="sxs-lookup"><span data-stu-id="b8e2a-120">Cancel</span></span></td>
<td><span data-ttu-id="b8e2a-121">Questo flag fa in modo che JetPrepareUpdate annulli l'aggiornamento per questo cursore.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-121">This flag causes JetPrepareUpdate to cancel the update for this cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b8e2a-122">ReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="b8e2a-122">ReplaceNoLock</span></span></td>
<td><span data-ttu-id="b8e2a-123">Questo flag è simile a JET_prepReplace, ma non viene effettuato alcun blocco per impedire ad altre sessioni di aggiornare questo record.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-123">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="b8e2a-124">Questa sessione può invece ricevere JET_errWriteConflict quando chiama JetUpdate per completare l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-124">Instead, this session may receive JET_errWriteConflict when it calls JetUpdate to complete the update.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="b8e2a-125">InsertCopy</span><span class="sxs-lookup"><span data-stu-id="b8e2a-125">InsertCopy</span></span></td>
<td><span data-ttu-id="b8e2a-126">Questo flag determina la preparazione del cursore per l'inserimento di una copia del record esistente.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-126">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="b8e2a-127">Se viene utilizzata questa opzione, deve essere presente un record corrente.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-127">There must be a current record if this option is used.</span></span> <span data-ttu-id="b8e2a-128">Lo stato iniziale del nuovo record viene copiato dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-128">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="b8e2a-129">I valori Long archiviati in modalità non registrata vengono copiati virtualmente.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-129">Long values that are stored off-record are virtually copied.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="b8e2a-130">InsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="b8e2a-130">InsertCopyDeleteOriginal</span></span></td>
<td><span data-ttu-id="b8e2a-131">Questo flag determina la preparazione del cursore per un inserimento dello stesso record e per l'eliminazione o il record originale.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-131">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="b8e2a-132">Viene utilizzato nei casi in cui la chiave primaria è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="b8e2a-132">It is used in cases in which the primary key has changed.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="b8e2a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8e2a-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8e2a-134">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b8e2a-134">Reference</span></span>

[<span data-ttu-id="b8e2a-135">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b8e2a-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
