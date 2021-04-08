---
description: 'Altre informazioni su: Proprietà JET_DBINFOMISC'
title: Proprietà JET_DBINFOMISC
TOCTitle: JET_DBINFOMISC properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc_properties(v=EXCHG.10)
ms:contentKeyID: 39515692
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 43f65126c3c257f2e0c9c7735348befa44198729
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749895"
---
# <a name="jet_dbinfomisc-properties"></a><span data-ttu-id="8808b-103">Proprietà JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="8808b-103">JET_DBINFOMISC properties</span></span>

<span data-ttu-id="8808b-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="8808b-104">Include protected members</span></span>  
<span data-ttu-id="8808b-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="8808b-105">Include inherited members</span></span>  

<span data-ttu-id="8808b-106">Il tipo di [JET_DBINFOMISC](./jet-dbinfomisc-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="8808b-106">The [JET_DBINFOMISC](./jet-dbinfomisc-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="8808b-107">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8808b-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="8808b-108">Nome</span><span class="sxs-lookup"><span data-stu-id="8808b-108">Name</span></span></th>
<th><span data-ttu-id="8808b-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8808b-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-111"><a href="hh578821(v=exchg.10).md">bkinfoCopyPrev</a></span><span class="sxs-lookup"><span data-stu-id="8808b-111"><a href="hh578821(v=exchg.10).md">bkinfoCopyPrev</a></span></span></td>
<td><span data-ttu-id="8808b-112">Ottiene informazioni sull'ultimo backup di copia riuscito.</span><span class="sxs-lookup"><span data-stu-id="8808b-112">Gets information about the last successful copy backup.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-114"><a href="hh565264(v=exchg.10).md">bkinfoDiffPrev</a></span><span class="sxs-lookup"><span data-stu-id="8808b-114"><a href="hh565264(v=exchg.10).md">bkinfoDiffPrev</a></span></span></td>
<td><span data-ttu-id="8808b-115">Ottiene informazioni sull'ultimo backup differenziale riuscito.</span><span class="sxs-lookup"><span data-stu-id="8808b-115">Gets information about the last successful differential backup.</span></span> <span data-ttu-id="8808b-116">Reimposta quando <a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a> è impostato.</span><span class="sxs-lookup"><span data-stu-id="8808b-116">Reset when <a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a> is set.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-118"><a href="hh577657(v=exchg.10).md">bkinfoFullCur</a></span><span class="sxs-lookup"><span data-stu-id="8808b-118"><a href="hh577657(v=exchg.10).md">bkinfoFullCur</a></span></span></td>
<td><span data-ttu-id="8808b-119">Ottiene informazioni sul backup corrente.</span><span class="sxs-lookup"><span data-stu-id="8808b-119">Gets information about the current backup.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-121"><a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a></span><span class="sxs-lookup"><span data-stu-id="8808b-121"><a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a></span></span></td>
<td><span data-ttu-id="8808b-122">Ottiene informazioni sull'ultimo backup completo completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="8808b-122">Gets information about the last successful full backup.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-124"><a href="hh564433(v=exchg.10).md">bkinfoIncPrev</a></span><span class="sxs-lookup"><span data-stu-id="8808b-124"><a href="hh564433(v=exchg.10).md">bkinfoIncPrev</a></span></span></td>
<td><span data-ttu-id="8808b-125">Ottiene informazioni sull'ultimo backup incrementale riuscito.</span><span class="sxs-lookup"><span data-stu-id="8808b-125">Gets information about the last successful incremental backup.</span></span> <span data-ttu-id="8808b-126">Questo valore viene reimpostato quando <a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a> è impostato.</span><span class="sxs-lookup"><span data-stu-id="8808b-126">This value is reset when <a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a> is set.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-128"><a href="hh578850(v=exchg.10).md">cbPageSize</a></span><span class="sxs-lookup"><span data-stu-id="8808b-128"><a href="hh578850(v=exchg.10).md">cbPageSize</a></span></span></td>
<td><span data-ttu-id="8808b-129">Ottiene le dimensioni della pagina del database.</span><span class="sxs-lookup"><span data-stu-id="8808b-129">Gets the database page size.</span></span> <span data-ttu-id="8808b-130">Il valore 0 indica le pagine 4Kb.</span><span class="sxs-lookup"><span data-stu-id="8808b-130">A value of 0 means 4Kb pages.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-132"><a href="hh558061(v=exchg.10).md">dbstate</a></span><span class="sxs-lookup"><span data-stu-id="8808b-132"><a href="hh558061(v=exchg.10).md">dbstate</a></span></span></td>
<td><span data-ttu-id="8808b-133">Ottiene lo stato coerente/incoerente del database.</span><span class="sxs-lookup"><span data-stu-id="8808b-133">Gets the consistent/inconsistent state of the database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-135"><a href="hh566598(v=exchg.10).md">dwBuildNumber</a></span><span class="sxs-lookup"><span data-stu-id="8808b-135"><a href="hh566598(v=exchg.10).md">dwBuildNumber</a></span></span></td>
<td><span data-ttu-id="8808b-136">Ottiene il numero di build del sistema operativo dall'ultima connessione.</span><span class="sxs-lookup"><span data-stu-id="8808b-136">Gets the OS build number from the last attach.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-138"><a href="hh578966(v=exchg.10).md">dwMajorVersion</a></span><span class="sxs-lookup"><span data-stu-id="8808b-138"><a href="hh578966(v=exchg.10).md">dwMajorVersion</a></span></span></td>
<td><span data-ttu-id="8808b-139">Ottiene la versione principale del sistema operativo dall'ultima connessione.</span><span class="sxs-lookup"><span data-stu-id="8808b-139">Gets the OS major version from the last attach.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-141"><a href="hh596571(v=exchg.10).md">dwMinorVersion</a></span><span class="sxs-lookup"><span data-stu-id="8808b-141"><a href="hh596571(v=exchg.10).md">dwMinorVersion</a></span></span></td>
<td><span data-ttu-id="8808b-142">Ottiene la versione secondaria del sistema operativo dall'ultima connessione.</span><span class="sxs-lookup"><span data-stu-id="8808b-142">Gets the OS minor version from the last attach.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-144"><a href="hh564660(v=exchg.10).md">fShadowingDisabled</a></span><span class="sxs-lookup"><span data-stu-id="8808b-144"><a href="hh564660(v=exchg.10).md">fShadowingDisabled</a></span></span></td>
<td><span data-ttu-id="8808b-145">Ottiene un valore che indica se l'ombreggiatura del catalogo è abilitata.</span><span class="sxs-lookup"><span data-stu-id="8808b-145">Gets a value indicating whether catalog shadowing is enabled.</span></span> <span data-ttu-id="8808b-146">Questo valore è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="8808b-146">This value is for internal use only.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-148"><a href="hh565757(v=exchg.10).md">fUpgradeDb</a></span><span class="sxs-lookup"><span data-stu-id="8808b-148"><a href="hh565757(v=exchg.10).md">fUpgradeDb</a></span></span></td>
<td><span data-ttu-id="8808b-149">Ottiene un valore che indica se il database è in fase di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="8808b-149">Gets a value indicating whether the database is being upgraded.</span></span> <span data-ttu-id="8808b-150">Questo valore è solo per uso interno.</span><span class="sxs-lookup"><span data-stu-id="8808b-150">This value is for internal use only.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-152"><a href="hh579055(v=exchg.10).md">genCommitted</a></span><span class="sxs-lookup"><span data-stu-id="8808b-152"><a href="hh579055(v=exchg.10).md">genCommitted</a></span></span></td>
<td><span data-ttu-id="8808b-153">Ottiene la generazione massima di log di cui è stato eseguito il commit nel database.</span><span class="sxs-lookup"><span data-stu-id="8808b-153">Gets the maximum log generation committed to the database.</span></span> <span data-ttu-id="8808b-154">In genere la generazione del log corrente.</span><span class="sxs-lookup"><span data-stu-id="8808b-154">Typically the current log generation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-156"><a href="hh579109(v=exchg.10).md">genMaxRequired</a></span><span class="sxs-lookup"><span data-stu-id="8808b-156"><a href="hh579109(v=exchg.10).md">genMaxRequired</a></span></span></td>
<td><span data-ttu-id="8808b-157">Ottiene la generazione massima di log necessaria per la riproduzione dei log.</span><span class="sxs-lookup"><span data-stu-id="8808b-157">Gets the maximum log generation required for replaying the logs.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-159"><a href="hh565891(v=exchg.10).md">genMinRequired</a></span><span class="sxs-lookup"><span data-stu-id="8808b-159"><a href="hh565891(v=exchg.10).md">genMinRequired</a></span></span></td>
<td><span data-ttu-id="8808b-160">Ottiene la generazione minima di log necessaria per la riproduzione dei log.</span><span class="sxs-lookup"><span data-stu-id="8808b-160">Gets the minimum log generation required for replaying the logs.</span></span> <span data-ttu-id="8808b-161">In genere la generazione del checkpoint.</span><span class="sxs-lookup"><span data-stu-id="8808b-161">Typically the checkpoint generation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-163"><a href="hh577443(v=exchg.10).md">lgposAttach</a></span><span class="sxs-lookup"><span data-stu-id="8808b-163"><a href="hh577443(v=exchg.10).md">lgposAttach</a></span></span></td>
<td><span data-ttu-id="8808b-164">Ottiene il LGPO dell'ultima connessione.</span><span class="sxs-lookup"><span data-stu-id="8808b-164">Gets the lgpos of the last attach.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-166"><a href="hh163307(v=exchg.10).md">lgposConsistent</a></span><span class="sxs-lookup"><span data-stu-id="8808b-166"><a href="hh163307(v=exchg.10).md">lgposConsistent</a></span></span></td>
<td><span data-ttu-id="8808b-167">Ottiene il LGPO quando il database è stato reso consistente.</span><span class="sxs-lookup"><span data-stu-id="8808b-167">Gets the lgpos when the database was made consistent.</span></span> <span data-ttu-id="8808b-168">Questo valore è null se il database è incoerente.</span><span class="sxs-lookup"><span data-stu-id="8808b-168">This value is null if the database is inconsistent.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-170"><a href="hh566733(v=exchg.10).md">lgposDetach</a></span><span class="sxs-lookup"><span data-stu-id="8808b-170"><a href="hh566733(v=exchg.10).md">lgposDetach</a></span></span></td>
<td><span data-ttu-id="8808b-171">Ottiene il LGPO dell'ultimo scollegamento.</span><span class="sxs-lookup"><span data-stu-id="8808b-171">Gets the lgpos of the last detach.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-173"><a href="hh564456(v=exchg.10).md">logtimeAttach</a></span><span class="sxs-lookup"><span data-stu-id="8808b-173"><a href="hh564456(v=exchg.10).md">logtimeAttach</a></span></span></td>
<td><span data-ttu-id="8808b-174">Ottiene l'ora in cui è stato collegato il database.</span><span class="sxs-lookup"><span data-stu-id="8808b-174">Gets the time when the database was attached.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-176"><a href="hh566711(v=exchg.10).md">logtimeBadChecksum</a></span><span class="sxs-lookup"><span data-stu-id="8808b-176"><a href="hh566711(v=exchg.10).md">logtimeBadChecksum</a></span></span></td>
<td><span data-ttu-id="8808b-177">Ottiene l'ultima volta in cui è stato trovato un errore di checksum non correggibile.</span><span class="sxs-lookup"><span data-stu-id="8808b-177">Gets the last time a non-correctable checksum error was found.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-179"><a href="hh557946(v=exchg.10).md">logtimeConsistent</a></span><span class="sxs-lookup"><span data-stu-id="8808b-179"><a href="hh557946(v=exchg.10).md">logtimeConsistent</a></span></span></td>
<td><span data-ttu-id="8808b-180">Ottiene l'ora in cui il database è stato reso consistente.</span><span class="sxs-lookup"><span data-stu-id="8808b-180">Gets the time when the database was made consistent.</span></span> <span data-ttu-id="8808b-181">Questo valore è null se il database è incoerente.</span><span class="sxs-lookup"><span data-stu-id="8808b-181">This value is null if the database is inconsistent.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-183"><a href="hh556940(v=exchg.10).md">logtimeDetach</a></span><span class="sxs-lookup"><span data-stu-id="8808b-183"><a href="hh556940(v=exchg.10).md">logtimeDetach</a></span></span></td>
<td><span data-ttu-id="8808b-184">Ottiene l'ora dell'ultima disconnessione.</span><span class="sxs-lookup"><span data-stu-id="8808b-184">Gets the time of the last detach.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-186"><a href="hh557356(v=exchg.10).md">logtimeECCFixFail</a></span><span class="sxs-lookup"><span data-stu-id="8808b-186"><a href="hh557356(v=exchg.10).md">logtimeECCFixFail</a></span></span></td>
<td><span data-ttu-id="8808b-187">Ottiene l'ultima volta in cui è stato rilevato un errore di un bit non correggibile.</span><span class="sxs-lookup"><span data-stu-id="8808b-187">Gets the last time an uncorrectable one bit error was encountered.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-189"><a href="hh578967(v=exchg.10).md">logtimeECCFixSuccess</a></span><span class="sxs-lookup"><span data-stu-id="8808b-189"><a href="hh578967(v=exchg.10).md">logtimeECCFixSuccess</a></span></span></td>
<td><span data-ttu-id="8808b-190">Ottiene l'ultima volta in cui è stato corretto un errore di un bit.</span><span class="sxs-lookup"><span data-stu-id="8808b-190">Gets the last time a one bit error was successfully fixed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-192"><a href="hh577625(v=exchg.10).md">logtimeGenMaxCreate</a></span><span class="sxs-lookup"><span data-stu-id="8808b-192"><a href="hh577625(v=exchg.10).md">logtimeGenMaxCreate</a></span></span></td>
<td><span data-ttu-id="8808b-193">Ottiene l'ora di creazione del file di log <a href="hh579109(v=exchg.10).md">genMaxRequired</a> .</span><span class="sxs-lookup"><span data-stu-id="8808b-193">Gets the creation time of the <a href="hh579109(v=exchg.10).md">genMaxRequired</a> logfile.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-195"><a href="hh579510(v=exchg.10).md">logtimeRepair</a></span><span class="sxs-lookup"><span data-stu-id="8808b-195"><a href="hh579510(v=exchg.10).md">logtimeRepair</a></span></span></td>
<td><span data-ttu-id="8808b-196">Ottiene l'ultima volta in cui è stato eseguito il ripristino sul database.</span><span class="sxs-lookup"><span data-stu-id="8808b-196">Gets the last time that repair was run against this database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-198"><a href="hh565142(v=exchg.10).md">lSPNumber</a></span><span class="sxs-lookup"><span data-stu-id="8808b-198"><a href="hh565142(v=exchg.10).md">lSPNumber</a></span></span></td>
<td><span data-ttu-id="8808b-199">Ottiene il numero del Service Pack del sistema operativo dall'ultima connessione.</span><span class="sxs-lookup"><span data-stu-id="8808b-199">Gets the OS Service Pack number from the last attach.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-201"><a href="hh564996(v=exchg.10).md">signDb</a></span><span class="sxs-lookup"><span data-stu-id="8808b-201"><a href="hh564996(v=exchg.10).md">signDb</a></span></span></td>
<td><span data-ttu-id="8808b-202">Ottiene la firma del database.</span><span class="sxs-lookup"><span data-stu-id="8808b-202">Gets the database signature.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-204"><a href="hh578351(v=exchg.10).md">signLog</a></span><span class="sxs-lookup"><span data-stu-id="8808b-204"><a href="hh578351(v=exchg.10).md">signLog</a></span></span></td>
<td><span data-ttu-id="8808b-205">Ottiene la firma logfile dei log utilizzati per modificare il database.</span><span class="sxs-lookup"><span data-stu-id="8808b-205">Gets the logfile signature of logs used to modify the database.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-207"><a href="hh596347(v=exchg.10).md">ulBadChecksum</a></span><span class="sxs-lookup"><span data-stu-id="8808b-207"><a href="hh596347(v=exchg.10).md">ulBadChecksum</a></span></span></td>
<td><span data-ttu-id="8808b-208">Ottiene il numero di volte in cui è stato trovato un errore di checksum non correggibile.</span><span class="sxs-lookup"><span data-stu-id="8808b-208">Gets the number of times a non-correctable checksum error was found.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-210"><a href="hh557876(v=exchg.10).md">ulBadChecksumOld</a></span><span class="sxs-lookup"><span data-stu-id="8808b-210"><a href="hh557876(v=exchg.10).md">ulBadChecksumOld</a></span></span></td>
<td><span data-ttu-id="8808b-211">Ottiene il numero di volte in cui è stato rilevato un errore di checksum non correggibile prima dell'ultimo ripristino.</span><span class="sxs-lookup"><span data-stu-id="8808b-211">Gets the number of times a non-correctable checksum error was found before the last repair.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-213"><a href="hh566254(v=exchg.10).md">ulECCFixFail</a></span><span class="sxs-lookup"><span data-stu-id="8808b-213"><a href="hh566254(v=exchg.10).md">ulECCFixFail</a></span></span></td>
<td><span data-ttu-id="8808b-214">Ottiene il numero di volte in cui è stato rilevato un errore di un bit non correggibile.</span><span class="sxs-lookup"><span data-stu-id="8808b-214">Gets the number of times an uncorrectable one bit error was encountered.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-216"><a href="hh564490(v=exchg.10).md">ulECCFixFailOld</a></span><span class="sxs-lookup"><span data-stu-id="8808b-216"><a href="hh564490(v=exchg.10).md">ulECCFixFailOld</a></span></span></td>
<td><span data-ttu-id="8808b-217">Ottiene il numero di volte in cui è stato rilevato un errore di un bit non correggibile.</span><span class="sxs-lookup"><span data-stu-id="8808b-217">Gets the number of times an uncorrectable one bit error was encountered.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-219"><a href="hh578574(v=exchg.10).md">ulECCFixSuccess</a></span><span class="sxs-lookup"><span data-stu-id="8808b-219"><a href="hh578574(v=exchg.10).md">ulECCFixSuccess</a></span></span></td>
<td><span data-ttu-id="8808b-220">Ottiene il numero di volte in cui un errore di un bit è stato corretto correttamente.</span><span class="sxs-lookup"><span data-stu-id="8808b-220">Gets the number of times a one bit error was successfully fixed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-222"><a href="hh578638(v=exchg.10).md">ulECCFixSuccessOld</a></span><span class="sxs-lookup"><span data-stu-id="8808b-222"><a href="hh578638(v=exchg.10).md">ulECCFixSuccessOld</a></span></span></td>
<td><span data-ttu-id="8808b-223">Ottiene il numero di volte in cui un errore di un bit è stato corretto prima dell'ultimo ripristino.</span><span class="sxs-lookup"><span data-stu-id="8808b-223">Gets the number of times a one bit error was successfully fixed before the last repair.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-225"><a href="hh579357(v=exchg.10).md">ulRepairCount</a></span><span class="sxs-lookup"><span data-stu-id="8808b-225"><a href="hh579357(v=exchg.10).md">ulRepairCount</a></span></span></td>
<td><span data-ttu-id="8808b-226">Ottiene il numero di volte in cui è stato chiamato il metodo Repair sul database.</span><span class="sxs-lookup"><span data-stu-id="8808b-226">Gets the number of times repair has been called on this database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-228"><a href="hh557020(v=exchg.10).md">ulRepairCountOld</a></span><span class="sxs-lookup"><span data-stu-id="8808b-228"><a href="hh557020(v=exchg.10).md">ulRepairCountOld</a></span></span></td>
<td><span data-ttu-id="8808b-229">Ottiene il numero di volte in cui il database è stato ripristinato prima dell'ultima deframmentazione.</span><span class="sxs-lookup"><span data-stu-id="8808b-229">Gets the number of times this database was repaired before the last defrag.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-231"><a href="hh596219(v=exchg.10).md">ulUpdate</a></span><span class="sxs-lookup"><span data-stu-id="8808b-231"><a href="hh596219(v=exchg.10).md">ulUpdate</a></span></span></td>
<td><span data-ttu-id="8808b-232">Ottiene la versione incrementale di ESENT che ha creato il database.</span><span class="sxs-lookup"><span data-stu-id="8808b-232">Gets the incremental version of Esent that created the database.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><span data-ttu-id="8808b-234"><a href="hh577854(v=exchg.10).md">ulVersion</a></span><span class="sxs-lookup"><span data-stu-id="8808b-234"><a href="hh577854(v=exchg.10).md">ulVersion</a></span></span></td>
<td><span data-ttu-id="8808b-235">Ottiene la versione di ESENT che ha creato il database.</span><span class="sxs-lookup"><span data-stu-id="8808b-235">Gets the version of Esent that created the database.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8808b-236">Inizio</span><span class="sxs-lookup"><span data-stu-id="8808b-236">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="8808b-237">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8808b-237">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8808b-238">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8808b-238">Reference</span></span>

[<span data-ttu-id="8808b-239">Classe JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="8808b-239">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="8808b-240">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8808b-240">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
