---
description: 'Altre informazioni su: struttura JET_DBINFOMISC3'
title: Struttura JET_DBINFOMISC3
TOCTitle: JET_DBINFOMISC3 Structure
ms:assetid: ffb23ac1-21ad-4dc6-98f8-aa4e6ef395ac
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294148(v=EXCHG.10)
ms:contentKeyID: 32765762
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 761afe13638d7905b5d4a639b7100108ce6ec977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226072"
---
# <a name="jet_dbinfomisc3-structure"></a><span data-ttu-id="b9be6-103">Struttura JET_DBINFOMISC3</span><span class="sxs-lookup"><span data-stu-id="b9be6-103">JET_DBINFOMISC3 Structure</span></span>


<span data-ttu-id="b9be6-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b9be6-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_dbinfomisc3-structure"></a><span data-ttu-id="b9be6-105">Struttura JET_DBINFOMISC3</span><span class="sxs-lookup"><span data-stu-id="b9be6-105">JET_DBINFOMISC3 Structure</span></span>

<span data-ttu-id="b9be6-106">La struttura **JET_DBINFOMISC3** include informazioni varie su un database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-106">The **JET_DBINFOMISC3** structure holds miscellaneous information about a database.</span></span> <span data-ttu-id="b9be6-107">Si tratta delle informazioni contenute nell'intestazione del database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-107">This is the information that is contained in the database header.</span></span>

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
      unsigned long genMinRequired;
      unsigned long genMaxRequired;
      JET_LOGTIME logtimeGenMaxCreate;
      unsigned long ulRepairCount;
      JET_LOGTIME logtimeRepair;
      unsigned long ulRepairCountOld;
      unsigned long ulECCFixSuccess;
      JET_LOGTIME logtimeECCFixSuccess;
      unsigned long ulECCFixSuccessOld;
      unsigned long ulECCFixFail;
      JET_LOGTIME logtimeECCFixFail;
      unsigned long ulECCFixFailOld;
      unsigned long ulBadChecksum;
      JET_LOGTIME logtimeBadChecksum;
      unsigned long ulBadChecksumOld;
      unsigned long genCommitted;
    } JET_DBINFOMISC3;
```

### <a name="members"></a><span data-ttu-id="b9be6-108">Membri</span><span class="sxs-lookup"><span data-stu-id="b9be6-108">Members</span></span>

<span data-ttu-id="b9be6-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="b9be6-109">**ulVersion**</span></span>

<span data-ttu-id="b9be6-110">Versione nativa del motore di database che ha creato il database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-110">The native version of the database engine that created the database.</span></span> <span data-ttu-id="b9be6-111">Vedere [JetGetVersion](./jetgetversion-function.md) per recuperare la versione nativa per il motore di database corrente.</span><span class="sxs-lookup"><span data-stu-id="b9be6-111">See [JetGetVersion](./jetgetversion-function.md) to retrieve the native version for the current database engine.</span></span>

<span data-ttu-id="b9be6-112">**ulUpdate**</span><span class="sxs-lookup"><span data-stu-id="b9be6-112">**ulUpdate**</span></span>

<span data-ttu-id="b9be6-113">Tiene traccia degli aggiornamenti del formato del database incrementale che sono compatibili con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="b9be6-113">Tracks incremental database format updates that are backward compatible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9be6-114">ulVersion, ulUpdate =</span><span class="sxs-lookup"><span data-stu-id="b9be6-114">ulVersion, ulUpdate =</span></span></p></th>
<th><p><span data-ttu-id="b9be6-115">Significato</span><span class="sxs-lookup"><span data-stu-id="b9be6-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-116">0x620, 0</span><span class="sxs-lookup"><span data-stu-id="b9be6-116">0x620,0</span></span></p></td>
<td><p><span data-ttu-id="b9be6-117">Formato beta originale del sistema operativo (4/22/97).</span><span class="sxs-lookup"><span data-stu-id="b9be6-117">Original operating system Beta format (4/22/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-118">0x620, 1</span><span class="sxs-lookup"><span data-stu-id="b9be6-118">0x620,1</span></span></p></td>
<td><p><span data-ttu-id="b9be6-119">Aggiungere le colonne nel catalogo per l'indicizzazione condizionale e quella precedente (5/29/97).</span><span class="sxs-lookup"><span data-stu-id="b9be6-119">Add columns in the catalog for conditional indexing and OLD (5/29/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-120">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="b9be6-120">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="b9be6-121">Aggiungere il flag fLocalizedText in IDB (6/5/97).</span><span class="sxs-lookup"><span data-stu-id="b9be6-121">Add the fLocalizedText flag in IDB (6/5/97).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-122">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="b9be6-122">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="b9be6-123">Aggiungere SPLIT_BUFFER alle pagine radice dell'albero dello spazio (10/30/97).</span><span class="sxs-lookup"><span data-stu-id="b9be6-123">Add SPLIT_BUFFER to space tree root pages (10/30/97).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-124">0x620, 2</span><span class="sxs-lookup"><span data-stu-id="b9be6-124">0x620,2</span></span></p></td>
<td><p><span data-ttu-id="b9be6-125">Ripristinare la revisione affinché ESE97 rimanga compatibile con le versioni successive (1/28/98).</span><span class="sxs-lookup"><span data-stu-id="b9be6-125">Revert revision in order for ESE97 to remain forward-compatible (1/28/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-126">0x620, 3</span><span class="sxs-lookup"><span data-stu-id="b9be6-126">0x620,3</span></span></p></td>
<td><p><span data-ttu-id="b9be6-127">Aggiungere nuove colonne con tag al catalogo ( &quot; CallbackData &quot; e &quot; CallbackDependencies &quot; ).</span><span class="sxs-lookup"><span data-stu-id="b9be6-127">Add new tagged columns to catalog (&quot;CallbackData&quot; and &quot;CallbackDependencies&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-128">0x620, 4</span><span class="sxs-lookup"><span data-stu-id="b9be6-128">0x620,4</span></span></p></td>
<td><p><span data-ttu-id="b9be6-129">Supporto di SLV: signSLV, fSLVExists nell'intestazione DB (5/5/98).</span><span class="sxs-lookup"><span data-stu-id="b9be6-129">SLV support: signSLV, fSLVExists in db header (5/5/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-130">0x620, 5</span><span class="sxs-lookup"><span data-stu-id="b9be6-130">0x620,5</span></span></p></td>
<td><p><span data-ttu-id="b9be6-131">Nuovo albero dello spazio SLV (5/29/98).</span><span class="sxs-lookup"><span data-stu-id="b9be6-131">New SLV space tree (5/29/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-132">0x620, 6</span><span class="sxs-lookup"><span data-stu-id="b9be6-132">0x620,6</span></span></p></td>
<td><p><span data-ttu-id="b9be6-133">Mappa dello spazio SLV (10/12/98).</span><span class="sxs-lookup"><span data-stu-id="b9be6-133">SLV space map (10/12/98).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-134">0x620, 7</span><span class="sxs-lookup"><span data-stu-id="b9be6-134">0x620,7</span></span></p></td>
<td><p><span data-ttu-id="b9be6-135">IDXSEG a 4 byte (12/10/98).</span><span class="sxs-lookup"><span data-stu-id="b9be6-135">4-byte IDXSEG (12/10/98).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-136">0x620, 8</span><span class="sxs-lookup"><span data-stu-id="b9be6-136">0x620,8</span></span></p></td>
<td><p><span data-ttu-id="b9be6-137">Nuovo formato di colonna modello (1/25/99).</span><span class="sxs-lookup"><span data-stu-id="b9be6-137">New template column format (1/25/99).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-138">0x620, 9</span><span class="sxs-lookup"><span data-stu-id="b9be6-138">0x620,9</span></span></p></td>
<td><p><span data-ttu-id="b9be6-139">Colonne modello ordinate (6/24/99).</span><span class="sxs-lookup"><span data-stu-id="b9be6-139">Sorted template columns (6/24/99).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-140">0x620, A</span><span class="sxs-lookup"><span data-stu-id="b9be6-140">0x620,A</span></span></p></td>
<td><p><span data-ttu-id="b9be6-141">Codebase unita (3/26/2003).</span><span class="sxs-lookup"><span data-stu-id="b9be6-141">Merged code base (3/26/2003).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-142">0x620, B</span><span class="sxs-lookup"><span data-stu-id="b9be6-142">0x620,B</span></span></p></td>
<td><p><span data-ttu-id="b9be6-143">Nuovo formato di checksum (1/08/2004).</span><span class="sxs-lookup"><span data-stu-id="b9be6-143">New checksum format (1/08/2004).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-144">0x620, C</span><span class="sxs-lookup"><span data-stu-id="b9be6-144">0x620,C</span></span></p></td>
<td><p><span data-ttu-id="b9be6-145">Aumento della lunghezza massima della chiave a 1000/2000 byte per le pagine 4/8KB (1/15/2004).</span><span class="sxs-lookup"><span data-stu-id="b9be6-145">Increased max key length to 1000/2000 bytes for 4/8kb pages (1/15/2004).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-146">0x620, D</span><span class="sxs-lookup"><span data-stu-id="b9be6-146">0x620,D</span></span></p></td>
<td><p><span data-ttu-id="b9be6-147">Hint dello spazio del catalogo space_header. V2 (7/15/2007).</span><span class="sxs-lookup"><span data-stu-id="b9be6-147">Catalog space hints, space_header.v2 (7/15/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-148">0x620, E</span><span class="sxs-lookup"><span data-stu-id="b9be6-148">0x620,E</span></span></p></td>
<td><p><span data-ttu-id="b9be6-149">Aggiungere il nuovo formato di nodo/extent a gestione spazio, usarlo per i pool di spazio riservati (8/9/2007).</span><span class="sxs-lookup"><span data-stu-id="b9be6-149">Add new node/extent format to space manager, use it for reserved pools of space (8/9/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-150">0x620, F</span><span class="sxs-lookup"><span data-stu-id="b9be6-150">0x620,F</span></span></p></td>
<td><p><span data-ttu-id="b9be6-151">Compressione per valori Long intrinseci (10/30/2007).</span><span class="sxs-lookup"><span data-stu-id="b9be6-151">Compression for intrinsic long-values (10/30/2007).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-152">0x620, 10</span><span class="sxs-lookup"><span data-stu-id="b9be6-152">0x620,10</span></span></p></td>
<td><p><span data-ttu-id="b9be6-153">Compressione per valori Long separati (12/05/2007).</span><span class="sxs-lookup"><span data-stu-id="b9be6-153">Compression for separated long-values (12/05/2007).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-154">0x620, 11</span><span class="sxs-lookup"><span data-stu-id="b9be6-154">0x620,11</span></span></p></td>
<td><p><span data-ttu-id="b9be6-155">Nuove dimensioni del blocco LV per pagine di grandi dimensioni (12/29/2007).</span><span class="sxs-lookup"><span data-stu-id="b9be6-155">New LV chunk size for large pages (12/29/2007).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9be6-156">**signDb**</span><span class="sxs-lookup"><span data-stu-id="b9be6-156">**signDb**</span></span>

<span data-ttu-id="b9be6-157">Firma del database (inclusa l'ora di creazione).</span><span class="sxs-lookup"><span data-stu-id="b9be6-157">Signature of the database (including creation time).</span></span> <span data-ttu-id="b9be6-158">Questa struttura è di 28 byte.</span><span class="sxs-lookup"><span data-stu-id="b9be6-158">This structure is 28 bytes.</span></span>

<span data-ttu-id="b9be6-159">**dbstate**</span><span class="sxs-lookup"><span data-stu-id="b9be6-159">**dbstate**</span></span>

<span data-ttu-id="b9be6-160">Si tratta dello stato del database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-160">This is the database state.</span></span>

<span data-ttu-id="b9be6-161">Per questo membro sono disponibili le opzioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="b9be6-161">The following options are available for this member.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b9be6-162">Valore</span><span class="sxs-lookup"><span data-stu-id="b9be6-162">Value</span></span></p></th>
<th><p><span data-ttu-id="b9be6-163">Significato</span><span class="sxs-lookup"><span data-stu-id="b9be6-163">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-164">JET_dbstateJustCreated</span><span class="sxs-lookup"><span data-stu-id="b9be6-164">JET_dbstateJustCreated</span></span><br />
<span data-ttu-id="b9be6-165">1</span><span class="sxs-lookup"><span data-stu-id="b9be6-165">1</span></span></p></td>
<td><p><span data-ttu-id="b9be6-166">Il database è stato appena creato.</span><span class="sxs-lookup"><span data-stu-id="b9be6-166">The database was just created.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-167">JET_dbstateDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="b9be6-167">JET_dbstateDirtyShutdown</span></span><br />
<span data-ttu-id="b9be6-168">2</span><span class="sxs-lookup"><span data-stu-id="b9be6-168">2</span></span></p></td>
<td><p><span data-ttu-id="b9be6-169">Il database richiede l'esecuzione di un ripristino software o hardware per poter essere utilizzato o spostabile.</span><span class="sxs-lookup"><span data-stu-id="b9be6-169">The database requires hard or soft recovery to be run in order to become usable or moveable.</span></span> <span data-ttu-id="b9be6-170">Non provare a spostare i database in questo stato.</span><span class="sxs-lookup"><span data-stu-id="b9be6-170">One should not try to move databases in this state.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-171">JET_dbstateCleanShutdown</span><span class="sxs-lookup"><span data-stu-id="b9be6-171">JET_dbstateCleanShutdown</span></span><br />
<span data-ttu-id="b9be6-172">3</span><span class="sxs-lookup"><span data-stu-id="b9be6-172">3</span></span></p></td>
<td><p><span data-ttu-id="b9be6-173">Il database è in uno stato pulito.</span><span class="sxs-lookup"><span data-stu-id="b9be6-173">The database is in a clean state.</span></span> <span data-ttu-id="b9be6-174">Il database può essere collegato senza file di log.</span><span class="sxs-lookup"><span data-stu-id="b9be6-174">The database can be attached without any log files.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-175">JET_dbstateBeingConverted</span><span class="sxs-lookup"><span data-stu-id="b9be6-175">JET_dbstateBeingConverted</span></span><br />
<span data-ttu-id="b9be6-176">4</span><span class="sxs-lookup"><span data-stu-id="b9be6-176">4</span></span></p></td>
<td><p><span data-ttu-id="b9be6-177">È in corso l'aggiornamento del database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-177">The database is being upgraded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-178">JET_dbstateForceDetach</span><span class="sxs-lookup"><span data-stu-id="b9be6-178">JET_dbstateForceDetach</span></span><br />
<span data-ttu-id="b9be6-179">5</span><span class="sxs-lookup"><span data-stu-id="b9be6-179">5</span></span></p></td>
<td><p><span data-ttu-id="b9be6-180">Interno.</span><span class="sxs-lookup"><span data-stu-id="b9be6-180">Internal.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b9be6-181">**lgposConsistent**</span><span class="sxs-lookup"><span data-stu-id="b9be6-181">**lgposConsistent**</span></span>

<span data-ttu-id="b9be6-182">Null se il database è in uno stato dirty.</span><span class="sxs-lookup"><span data-stu-id="b9be6-182">Null if the database is in a dirty state.</span></span> <span data-ttu-id="b9be6-183">Si tratta della posizione del log utilizzata quando il database è stato portato per l'ultima volta a uno stato di chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="b9be6-183">This is the log position that was used when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="b9be6-184">**logtimeConsistent**</span><span class="sxs-lookup"><span data-stu-id="b9be6-184">**logtimeConsistent**</span></span>

<span data-ttu-id="b9be6-185">Null se il database è in uno stato dirty.</span><span class="sxs-lookup"><span data-stu-id="b9be6-185">Null if the database is in a dirty state.</span></span> <span data-ttu-id="b9be6-186">Si tratta dell'ora in cui il database è stato portato per l'ultima volta a uno stato di chiusura normale.</span><span class="sxs-lookup"><span data-stu-id="b9be6-186">This is the time when the database was last brought to a clean shutdown state.</span></span>

<span data-ttu-id="b9be6-187">**logtimeAttach**</span><span class="sxs-lookup"><span data-stu-id="b9be6-187">**logtimeAttach**</span></span>

<span data-ttu-id="b9be6-188">Ora dell'ultima connessione del database con [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="b9be6-188">The time when the database was last attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="b9be6-189">**lgposAttach**</span><span class="sxs-lookup"><span data-stu-id="b9be6-189">**lgposAttach**</span></span>

<span data-ttu-id="b9be6-190">Posizione del log utilizzata per l'ultima volta che il database è stato collegato a [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="b9be6-190">The log position that was used the last time the database was attached with [JetAttachDatabase](./jetattachdatabase-function.md).</span></span>

<span data-ttu-id="b9be6-191">**logtimeDetach**</span><span class="sxs-lookup"><span data-stu-id="b9be6-191">**logtimeDetach**</span></span>

<span data-ttu-id="b9be6-192">Data e ora dell'ultimo scollegamento del database con [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="b9be6-192">The time when the database was last detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="b9be6-193">**lgposDetach**</span><span class="sxs-lookup"><span data-stu-id="b9be6-193">**lgposDetach**</span></span>

<span data-ttu-id="b9be6-194">Posizione del log utilizzata per l'ultima volta in cui il database è stato scollegato con [JetDetachDatabase](./jetdetachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="b9be6-194">The log position that was used the last time the database was detached with [JetDetachDatabase](./jetdetachdatabase-function.md).</span></span>

<span data-ttu-id="b9be6-195">**signLog**</span><span class="sxs-lookup"><span data-stu-id="b9be6-195">**signLog**</span></span>

<span data-ttu-id="b9be6-196">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="b9be6-196">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="b9be6-197">**bkinfoFullPrev**</span><span class="sxs-lookup"><span data-stu-id="b9be6-197">**bkinfoFullPrev**</span></span>

<span data-ttu-id="b9be6-198">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="b9be6-198">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="b9be6-199">**bkinfoIncPrev**</span><span class="sxs-lookup"><span data-stu-id="b9be6-199">**bkinfoIncPrev**</span></span>

<span data-ttu-id="b9be6-200">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="b9be6-200">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="b9be6-201">**bkinfoFullCur**</span><span class="sxs-lookup"><span data-stu-id="b9be6-201">**bkinfoFullCur**</span></span>

<span data-ttu-id="b9be6-202">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="b9be6-202">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="b9be6-203">**fShadowingDisabled**</span><span class="sxs-lookup"><span data-stu-id="b9be6-203">**fShadowingDisabled**</span></span>

<span data-ttu-id="b9be6-204">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="b9be6-204">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="b9be6-205">**fUpgradeDb**</span><span class="sxs-lookup"><span data-stu-id="b9be6-205">**fUpgradeDb**</span></span>

<span data-ttu-id="b9be6-206">Supporta l'infrastruttura ESE e non può essere utilizzato nel codice.</span><span class="sxs-lookup"><span data-stu-id="b9be6-206">Supports the ESE infrastructure and cannot be used in your code.</span></span>

<span data-ttu-id="b9be6-207">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="b9be6-207">**dwMajorVersion**</span></span>

<span data-ttu-id="b9be6-208">Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-208">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="b9be6-209">Utilizzato per l'aggiornamento degli indici.</span><span class="sxs-lookup"><span data-stu-id="b9be6-209">Used for updating indexes.</span></span>

<span data-ttu-id="b9be6-210">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="b9be6-210">**dwMinorVersion**</span></span>

<span data-ttu-id="b9be6-211">Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-211">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="b9be6-212">Utilizzato per l'aggiornamento degli indici.</span><span class="sxs-lookup"><span data-stu-id="b9be6-212">Used for updating indexes.</span></span>

<span data-ttu-id="b9be6-213">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="b9be6-213">**dwBuildNumber**</span></span>

<span data-ttu-id="b9be6-214">Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-214">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="b9be6-215">Utilizzato per l'aggiornamento degli indici.</span><span class="sxs-lookup"><span data-stu-id="b9be6-215">Used for updating indexes.</span></span>

<span data-ttu-id="b9be6-216">**lSPNumber**</span><span class="sxs-lookup"><span data-stu-id="b9be6-216">**lSPNumber**</span></span>

<span data-ttu-id="b9be6-217">Rappresenta i numeri di versione di Windows NT durante l'aggiornamento degli indici dei database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-217">Represents the Windows NT version numbers when the databases indexes were updated.</span></span> <span data-ttu-id="b9be6-218">Utilizzato per l'aggiornamento degli indici.</span><span class="sxs-lookup"><span data-stu-id="b9be6-218">Used for updating indexes.</span></span>

<span data-ttu-id="b9be6-219">**cbPageSize**</span><span class="sxs-lookup"><span data-stu-id="b9be6-219">**cbPageSize**</span></span>

<span data-ttu-id="b9be6-220">Dimensioni di pagina del database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-220">Database page size.</span></span> <span data-ttu-id="b9be6-221">0 indica che le dimensioni della pagina sono pari a 4 KB.</span><span class="sxs-lookup"><span data-stu-id="b9be6-221">0 means the page size is 4 KB.</span></span>

<span data-ttu-id="b9be6-222">Questo valore viene recuperato solo se JET_DbInfoMisc è stato passato a [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) o [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="b9be6-222">This value is retrieved only if JET_DbInfoMisc was passed to [JetGetDatabaseInfo](./jetgetdatabaseinfo-function.md) or [JetGetDatabaseFileInfo](./jetgetdatabasefileinfo-function.md).</span></span>

<span data-ttu-id="b9be6-223">**genMinRequired**</span><span class="sxs-lookup"><span data-stu-id="b9be6-223">**genMinRequired**</span></span>

<span data-ttu-id="b9be6-224">Rappresenta la generazione minima di log necessaria per la riproduzione dei log.</span><span class="sxs-lookup"><span data-stu-id="b9be6-224">Represents the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="b9be6-225">Questa operazione è in genere identica alla generazione del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="b9be6-225">This is typically the same as the checkpoint generation.</span></span>

<span data-ttu-id="b9be6-226">**genMaxRequired**</span><span class="sxs-lookup"><span data-stu-id="b9be6-226">**genMaxRequired**</span></span>

<span data-ttu-id="b9be6-227">Rappresenta la generazione massima di log necessaria per la riproduzione dei log.</span><span class="sxs-lookup"><span data-stu-id="b9be6-227">Represents the maximum log generation required for replaying the logs.</span></span>

<span data-ttu-id="b9be6-228">**logtimeGenMaxCreate**</span><span class="sxs-lookup"><span data-stu-id="b9be6-228">**logtimeGenMaxCreate**</span></span>

<span data-ttu-id="b9be6-229">Rappresenta la data e l'ora di creazione del file di log genMax.</span><span class="sxs-lookup"><span data-stu-id="b9be6-229">Represents the creation date and time of the genMax log file.</span></span>

<span data-ttu-id="b9be6-230">**ulRepairCount**</span><span class="sxs-lookup"><span data-stu-id="b9be6-230">**ulRepairCount**</span></span>

<span data-ttu-id="b9be6-231">Numero di volte in cui è stata richiamata una riparazione su questo database.</span><span class="sxs-lookup"><span data-stu-id="b9be6-231">The number of times a repair has been called on this database.</span></span>

<span data-ttu-id="b9be6-232">**logtimeRepair**</span><span class="sxs-lookup"><span data-stu-id="b9be6-232">**logtimeRepair**</span></span>

<span data-ttu-id="b9be6-233">Rappresenta la data e l'ora in cui è stato eseguito l'ultimo ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9be6-233">Represents the date and time the last repair was run.</span></span>

<span data-ttu-id="b9be6-234">**ulRepairCountOld**</span><span class="sxs-lookup"><span data-stu-id="b9be6-234">**ulRepairCountOld**</span></span>

<span data-ttu-id="b9be6-235">Il numero di volte in cui la riparazione è stata eseguita nel database prima dell'ultima deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="b9be6-235">The number of times the repair had been run on this database before the last defragmentation.</span></span>

<span data-ttu-id="b9be6-236">**ulECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="b9be6-236">**ulECCFixSuccess**</span></span>

<span data-ttu-id="b9be6-237">Il numero di volte in cui è stato corretto un errore di un bit che ha generato una pagina corretta.</span><span class="sxs-lookup"><span data-stu-id="b9be6-237">The number of times a one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="b9be6-238">**logtimeECCFixSuccess**</span><span class="sxs-lookup"><span data-stu-id="b9be6-238">**logtimeECCFixSuccess**</span></span>

<span data-ttu-id="b9be6-239">Rappresenta la data e l'ora in cui è stato corretto l'ultimo errore di un bit ed è stata generata una pagina corretta.</span><span class="sxs-lookup"><span data-stu-id="b9be6-239">Represents the date and time the last one bit error was fixed and resulted in a good page.</span></span>

<span data-ttu-id="b9be6-240">**ulECCFixSuccessOld**</span><span class="sxs-lookup"><span data-stu-id="b9be6-240">**ulECCFixSuccessOld**</span></span>

<span data-ttu-id="b9be6-241">Rappresenta il numero di volte in cui è stato corretto un errore di un bit e ha generato una pagina corretta prima dell'ultima correzione.</span><span class="sxs-lookup"><span data-stu-id="b9be6-241">Represents the number of times a one bit error was fixed and resulted in a good page before last repair.</span></span>

<span data-ttu-id="b9be6-242">**ulECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="b9be6-242">**ulECCFixFail**</span></span>

<span data-ttu-id="b9be6-243">Il numero di volte in cui è stato corretto un errore di un bit e il risultato è una pagina non valida.</span><span class="sxs-lookup"><span data-stu-id="b9be6-243">The number of times a one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="b9be6-244">**logtimeECCFixFail**</span><span class="sxs-lookup"><span data-stu-id="b9be6-244">**logtimeECCFixFail**</span></span>

<span data-ttu-id="b9be6-245">Rappresenta la data e l'ora in cui è stato corretto l'ultimo errore di un bit ed è stata generata una pagina non valida.</span><span class="sxs-lookup"><span data-stu-id="b9be6-245">Represents the date and time the last one bit error was fixed and resulted in a bad page.</span></span>

<span data-ttu-id="b9be6-246">**ulECCFixFailOld**</span><span class="sxs-lookup"><span data-stu-id="b9be6-246">**ulECCFixFailOld**</span></span>

<span data-ttu-id="b9be6-247">Il numero di volte in cui è stato corretto un errore di un bit che ha generato una pagina errata prima dell'ultima correzione.</span><span class="sxs-lookup"><span data-stu-id="b9be6-247">The number of times a one bit error was fixed and resulted in a bad page before last repair.</span></span>

<span data-ttu-id="b9be6-248">**ulBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="b9be6-248">**ulBadChecksum**</span></span>

<span data-ttu-id="b9be6-249">Il numero di volte in cui è stato trovato un errore ECC/checksum non correggibile.</span><span class="sxs-lookup"><span data-stu-id="b9be6-249">The number of times a non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="b9be6-250">**logtimeBadChecksum**</span><span class="sxs-lookup"><span data-stu-id="b9be6-250">**logtimeBadChecksum**</span></span>

<span data-ttu-id="b9be6-251">Rappresenta la data e l'ora in cui è stato rilevato l'ultimo errore ECC/checksum non correggibile.</span><span class="sxs-lookup"><span data-stu-id="b9be6-251">Represents the date and time the last non-correctable ECC/checksum error was found.</span></span>

<span data-ttu-id="b9be6-252">**ulBadChecksumOld**</span><span class="sxs-lookup"><span data-stu-id="b9be6-252">**ulBadChecksumOld**</span></span>

<span data-ttu-id="b9be6-253">Il numero di volte in cui è stato trovato un errore ECC/checksum non correggibile prima dell'ultimo ripristino.</span><span class="sxs-lookup"><span data-stu-id="b9be6-253">The number of times a non-correctable ECC/checksum error was found before last repair.</span></span>

<span data-ttu-id="b9be6-254">**genCommitted**</span><span class="sxs-lookup"><span data-stu-id="b9be6-254">**genCommitted**</span></span>

<span data-ttu-id="b9be6-255">Generazione del log corrente.</span><span class="sxs-lookup"><span data-stu-id="b9be6-255">The current log generation.</span></span> <span data-ttu-id="b9be6-256">Può essere minore di genMaxRequired se JET_paramWaypointLatency è diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="b9be6-256">This can be less than genMaxRequired if JET_paramWaypointLatency is non-zero.</span></span>

### <a name="requirements"></a><span data-ttu-id="b9be6-257">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9be6-257">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-258"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="b9be6-258"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b9be6-259">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b9be6-259">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b9be6-260"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b9be6-260"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b9be6-261">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b9be6-261">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b9be6-262"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="b9be6-262"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b9be6-263">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="b9be6-263">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b9be6-264">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="b9be6-264">See Also</span></span>

[<span data-ttu-id="b9be6-265">JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="b9be6-265">JET_BKINFO</span></span>](./jet-bkinfo-structure.md)  
[<span data-ttu-id="b9be6-266">JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="b9be6-266">JET_LOGTIME</span></span>](./jet-logtime-structure.md)  
[<span data-ttu-id="b9be6-267">JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="b9be6-267">JET_LGPOS</span></span>](./jet-lgpos-structure.md)  
[<span data-ttu-id="b9be6-268">JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="b9be6-268">JET_SIGNATURE</span></span>](./jet-signature-structure.md)  
[<span data-ttu-id="b9be6-269">JetGetDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="b9be6-269">JetGetDatabaseInfo</span></span>](./jetgetdatabaseinfo-function.md)  
[<span data-ttu-id="b9be6-270">JetGetDatabaseFileInfo</span><span class="sxs-lookup"><span data-stu-id="b9be6-270">JetGetDatabaseFileInfo</span></span>](./jetgetdatabasefileinfo-function.md)
