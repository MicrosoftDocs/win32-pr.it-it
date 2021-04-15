---
description: 'Altre informazioni su: struttura JET_DBINFOMISC'
title: Struttura JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC Structure
ms:assetid: ff287087-35b8-495e-9922-418ec2439e19
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294147(v=EXCHG.10)
ms:contentKeyID: 32765761
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 649e16e956e5dcd272e6201f779cdddd352a7bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525051"
---
# <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="c5494-103">Struttura JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="c5494-103">JET_DBINFOMISC Structure</span></span>


<span data-ttu-id="c5494-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c5494-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc-structure"></a><span data-ttu-id="c5494-105">Struttura JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="c5494-105">JET_DBINFOMISC Structure</span></span>

<span data-ttu-id="c5494-106">La struttura **JET_DBINFOMISC** include informazioni varie su un database.</span><span class="sxs-lookup"><span data-stu-id="c5494-106">The **JET_DBINFOMISC** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="c5494-107">Si tratta delle informazioni contenute nell'intestazione del database.</span><span class="sxs-lookup"><span data-stu-id="c5494-107">This is the information that is contained in the database header.</span></span>

```cpp
    typedef struct {
      unsigned long ulVersion;
      unsigned long ulUpdate;
      JET_SIGNATURE signDb;
      unsigned long dbstate;
      JET_LGPOS lgposConsistent;
      JET_LOGTIME logtimeConsistent;
      JET_LOGTIME logtimeAttach;
      JET_LGPOS lgposAttach;
      JET_LOGTIME logtimeDetach;
      JET_LGPOS lgposDetach;
      JET_SIGNATURE signLog;
      JET_BKINFO bkinfoFullPrev;
      JET_BKINFO bkinfoIncPrev;
      JET_BKINFO bkinfoFullCur;
      unsigned long fShadowingDisabled;
      unsigned long fUpgradeDb;
      unsigned long dwMajorVersion;
      unsigned long dwMinorVersion;
      unsigned long dwBuildNumber;
      long lSPNumber;
      unsigned long cbPageSize;
    } JET_DBINFOMISC;
```

### <a name="members"></a><span data-ttu-id="c5494-108">Membri</span><span class="sxs-lookup"><span data-stu-id="c5494-108">Members</span></span>

<span data-ttu-id="c5494-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="c5494-109">**ulVersion**</span></span>

<span data-ttu-id="c5494-110">Versione nativa del motore di database che ha creato il database.</span><span class="sxs-lookup"><span data-stu-id="c5494-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="c5494-111">Vedere [JetGetVersion](./jetgetversion-function.md) per recuperare la versione nativa per il motore di database corrente.</span><span class="sxs-lookup"><span data-stu-id="c5494-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="c5494-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="c5494-112">**ulUpdate**</span></span>

<span data-ttu-id="c5494-113">Tiene traccia degli aggiornamenti del formato del database incrementale che sono compatibili con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="c5494-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5494-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="c5494-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="c5494-115">Significato</span><span class="sxs-lookup"><span data-stu-id="c5494-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5494-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="c5494-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="c5494-117">Formato beta originale del sistema operativo (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="c5494-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5494-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="c5494-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="c5494-119">Aggiungere le colonne nel catalogo per l'indicizzazione condizionale e quella precedente (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="c5494-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5494-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="c5494-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="c5494-121">Aggiungere il flag fLocalizedText in IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="c5494-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5494-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="c5494-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="c5494-123">Aggiungere SPLIT_BUFFER alle pagine radice dell'albero dello spazio (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="c5494-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5494-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="c5494-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="c5494-125">Ripristinare la revisione affinché ESE97 rimanga compatibile con le versioni successive (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="c5494-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5494-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="c5494-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="c5494-127">Aggiungere nuove colonne con tag al catalogo ( &quot; CallbackData &quot; e &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="c5494-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5494-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="c5494-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="c5494-129">Supporto di SLV: signSLV, fSLVExists nell'intestazione DB (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="c5494-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5494-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="c5494-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="c5494-131">Nuovo albero dello spazio SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="c5494-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5494-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="c5494-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="c5494-133">Mappa dello spazio SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="c5494-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5494-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="c5494-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="c5494-135">IDXSEG a 4 byte (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="c5494-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5494-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="c5494-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="c5494-137">Nuovo formato di colonna modello (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="c5494-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5494-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="c5494-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="c5494-139">Colonne modello ordinate (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="c5494-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5494-140">0x623, 0</span><span class="sxs-lookup"><span data-stu-id="c5494-140">0x623,0</span></span></p></td>
<td><p><span data-ttu-id="c5494-141">Nuovo gestore dello spazio (5/15/99).</span><span class="sxs-lookup"><span data-stu-id="c5494-141">New Space Manager (5/15/99).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5494-142">**signDb**</span><span class="sxs-lookup"><span data-stu-id="c5494-142">**signDb**</span></span>

<span data-ttu-id="c5494-143">Firma del database (inclusa l'ora di creazione).</span><span class="sxs-lookup"><span data-stu-id="c5494-143">Signature of the database (including creation time).</span></span> <span data-ttu-id="c5494-144">Questa struttura è di 28 byte.</span><span class="sxs-lookup"><span data-stu-id="c5494-144">This structure is 28 bytes.</span></span>

<span data-ttu-id="c5494-145">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="c5494-145">**dbstate**</span></span>

<span data-ttu-id="c5494-146">Si tratta dello stato del database.</span><span class="sxs-lookup"><span data-stu-id="c5494-146">This is the database state.</span></span>

<span data-ttu-id="c5494-147">Per questo membro sono disponibili le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="c5494-147">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5494-148">Valore</span><span class="sxs-lookup"><span data-stu-id="c5494-148">Value</span></span></p></th>
<th><p><span data-ttu-id="c5494-149">Significato</span><span class="sxs-lookup"><span data-stu-id="c5494-149">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5494-150">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="c5494-150">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="c5494-151">1</span><span class="sxs-lookup"><span data-stu-id="c5494-151">1</span></span></p></td>
<td><p><span data-ttu-id="c5494-152">Il database è stato appena creato.</span><span class="sxs-lookup"><span data-stu-id="c5494-152">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5494-153">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="c5494-153">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="c5494-154">2</span><span class="sxs-lookup"><span data-stu-id="c5494-154">2</span></span></p></td>
<td><p><span data-ttu-id="c5494-155">Il database richiede l'esecuzione di un ripristino software o hardware per poter essere utilizzato o spostabile.</span><span class="sxs-lookup"><span data-stu-id="c5494-155">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="c5494-156">Non provare a spostare i database in questo stato.</span><span class="sxs-lookup"><span data-stu-id="c5494-156">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5494-157">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="c5494-157">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="c5494-158">3</span><span class="sxs-lookup"><span data-stu-id="c5494-158">3</span></span></p></td>
<td><p><span data-ttu-id="c5494-159">Il database è in uno stato pulito.</span><span class="sxs-lookup"><span data-stu-id="c5494-159">The database is in a clean state.</span></span> <span data-ttu-id="c5494-160">Il database può essere collegato senza file di log.</span><span class="sxs-lookup"><span data-stu-id="c5494-160">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5494-161">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="c5494-161">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="c5494-162">4</span><span class="sxs-lookup"><span data-stu-id="c5494-162">4</span></span></p></td>
<td><p><span data-ttu-id="c5494-163">È in corso l'aggiornamento del database.</span><span class="sxs-lookup"><span data-stu-id="c5494-163">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5494-164">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="c5494-164">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="c5494-165">5</span><span class="sxs-lookup"><span data-stu-id="c5494-165">5</span></span></p></td>
<td><p><span data-ttu-id="c5494-166">Interno.</span><span class="sxs-lookup"><span data-stu-id="c5494-166">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5494-167">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="c5494-167">**lgposConsistent**</span></span>

<span data-ttu-id="c5494-168">Null se il database è in uno stato dirty.</span><span class="sxs-lookup"><span data-stu-id="c5494-168">Null if the database is in a dirty state.</span></span> <span data-ttu-id="c5494-169">Si tratta della posizione del log utilizzata quando il database è stato portato per l'ultima volta a uno stato di chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="c5494-169">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="c5494-170">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="c5494-170">**logtimeConsistent**</span></span>

<span data-ttu-id="c5494-171">Null se il database è in uno stato dirty.</span><span class="sxs-lookup"><span data-stu-id="c5494-171">Null if the database is in a dirty state.</span></span> <span data-ttu-id="c5494-172">Si tratta dell'ora in cui il database è stato portato per l'ultima volta a uno stato di chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="c5494-172">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="c5494-173">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="c5494-173">**logtimeAttach**</span></span>

<span data-ttu-id="c5494-174">Ora dell'ultima connessione del database con [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5494-174">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="c5494-175">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="c5494-175">**lgposAttach**</span></span>

<span data-ttu-id="c5494-176">Posizione del log utilizzata per l'ultima volta che il database è stato collegato a [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5494-176">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="c5494-177">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="c5494-177">**logtimeDetach**</span></span>

<span data-ttu-id="c5494-178">Data e ora dell'ultimo scollegamento del database con [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5494-178">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="c5494-179">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="c5494-179">**lgposDetach**</span></span>

<span data-ttu-id="c5494-180">Posizione del log utilizzata per l'ultima volta in cui il database è stato scollegato con [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5494-180">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="c5494-181">**signLog**</span><span class="sxs-lookup"><span data-stu-id="c5494-181">**signLog**</span></span>

<span data-ttu-id="c5494-182">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="c5494-182">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="c5494-183">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="c5494-183">**bkinfoFullPrev**</span></span>

<span data-ttu-id="c5494-184">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="c5494-184">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="c5494-185">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="c5494-185">**bkinfoIncPrev**</span></span>

<span data-ttu-id="c5494-186">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="c5494-186">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="c5494-187">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="c5494-187">**bkinfoFullCur**</span></span>

<span data-ttu-id="c5494-188">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="c5494-188">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="c5494-189">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="c5494-189">**fShadowingDisabled**</span></span>

<span data-ttu-id="c5494-190">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="c5494-190">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="c5494-191">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="c5494-191">**fUpgradeDb**</span></span>

<span data-ttu-id="c5494-192">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="c5494-192">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="c5494-193">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="c5494-193">**dwMajorVersion**</span></span>

<span data-ttu-id="c5494-194">Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database.</span><span class="sxs-lookup"><span data-stu-id="c5494-194">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="c5494-195">Utilizzato per l'aggiornamento degli indici.</span><span class="sxs-lookup"><span data-stu-id="c5494-195">Used for updating indexes.</span></span>

<span data-ttu-id="c5494-196">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="c5494-196">**dwMinorVersion**</span></span>

<span data-ttu-id="c5494-197">Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database.</span><span class="sxs-lookup"><span data-stu-id="c5494-197">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="c5494-198">Utilizzato per l'aggiornamento degli indici.</span><span class="sxs-lookup"><span data-stu-id="c5494-198">Used for updating indexes.</span></span>

<span data-ttu-id="c5494-199">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="c5494-199">**dwBuildNumber**</span></span>

<span data-ttu-id="c5494-200">Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database.</span><span class="sxs-lookup"><span data-stu-id="c5494-200">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="c5494-201">Utilizzato per l'aggiornamento degli indici.</span><span class="sxs-lookup"><span data-stu-id="c5494-201">Used for updating indexes.</span></span>

<span data-ttu-id="c5494-202">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="c5494-202">**lSPNumber**</span></span>

<span data-ttu-id="c5494-203">Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database.</span><span class="sxs-lookup"><span data-stu-id="c5494-203">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="c5494-204">Utilizzato per l'aggiornamento degli indici.</span><span class="sxs-lookup"><span data-stu-id="c5494-204">Used for updating indexes.</span></span>

<span data-ttu-id="c5494-205">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="c5494-205">**cbPageSize**</span></span>

<span data-ttu-id="c5494-206">Dimensioni di pagina del database.</span><span class="sxs-lookup"><span data-stu-id="c5494-206">Database page size.</span></span> <span data-ttu-id="c5494-207">0 indica che le dimensioni della pagina sono pari a 4 KB.</span><span class="sxs-lookup"><span data-stu-id="c5494-207">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="c5494-208">Questo valore viene recuperato solo se JET_DbInfoMisc è stato passato a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="c5494-208">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="c5494-209">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5494-209">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5494-210"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c5494-210"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c5494-211">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c5494-211">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5494-212"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c5494-212"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c5494-213">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c5494-213">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5494-214"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c5494-214"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c5494-215">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c5494-215">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c5494-216">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c5494-216">See Also</span></span>

[<span data-ttu-id="c5494-217">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="c5494-217">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="c5494-218">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="c5494-218">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="c5494-219">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="c5494-219">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="c5494-220">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="c5494-220">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="c5494-221">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="c5494-221">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="c5494-222">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="c5494-222">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
