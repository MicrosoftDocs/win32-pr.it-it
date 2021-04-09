---
description: 'Altre informazioni su: membri di VistaParam'
title: Membri di VistaParam (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: VistaParam members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_members(v=EXCHG.10)
ms:contentKeyID: 55104333
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c56c8ad3a64eb08654ee893e86683e95e32af443
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878573"
---
# <a name="vistaparam-members"></a><span data-ttu-id="f1064-103">Membri di VistaParam</span><span class="sxs-lookup"><span data-stu-id="f1064-103">VistaParam members</span></span>

<span data-ttu-id="f1064-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="f1064-104">Include protected members</span></span>  
<span data-ttu-id="f1064-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="f1064-105">Include inherited members</span></span>  

<span data-ttu-id="f1064-106">Parametri di sistema aggiunti alla versione di vista di ESENT.</span><span class="sxs-lookup"><span data-stu-id="f1064-106">System parameters that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="f1064-107">Il tipo [VistaParam](./vistaparam-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="f1064-107">The [VistaParam](./vistaparam-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="f1064-108">Campi</span><span class="sxs-lookup"><span data-stu-id="f1064-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="f1064-109">Nome</span><span class="sxs-lookup"><span data-stu-id="f1064-109">Name</span></span></th>
<th><span data-ttu-id="f1064-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1064-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-113"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span><span class="sxs-lookup"><span data-stu-id="f1064-113"><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></span></span></td>
<td><span data-ttu-id="f1064-114">Questo parametro controlla il numero di risorse dell'albero B + memorizzato nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f1064-114">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="f1064-115">I valori di grandi dimensioni per questo parametro comportano l'utilizzo di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui l'applicazione può aprire in modo casuale un numero elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="f1064-115">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="f1064-116">Questa operazione è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.</span><span class="sxs-lookup"><span data-stu-id="f1064-116">This is useful for applications that have a schema with a very large number of tables.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-119"><a href="dn335289(v=exchg.10).md">Configuration</a></span><span class="sxs-lookup"><span data-stu-id="f1064-119"><a href="dn335289(v=exchg.10).md">Configuration</a></span></span></td>
<td><span data-ttu-id="f1064-120">Questo parametro espone più set di valori predefiniti per l'intero set di parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="f1064-120">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="f1064-121">Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione.</span><span class="sxs-lookup"><span data-stu-id="f1064-121">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="f1064-122">Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="f1064-122">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span> <span data-ttu-id="f1064-123">Small Configuration (0): il motore di database è ottimizzato per l'uso della memoria.</span><span class="sxs-lookup"><span data-stu-id="f1064-123">Small Configuration (0): The database engine is optimized for memory use.</span></span> <span data-ttu-id="f1064-124">Configurazione legacy (1): il motore di database presenta le impostazioni predefinite tradizionali.</span><span class="sxs-lookup"><span data-stu-id="f1064-124">Legacy Configuration (1): The database engine has its traditional defaults.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-127"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span><span class="sxs-lookup"><span data-stu-id="f1064-127"><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></span></span></td>
<td><span data-ttu-id="f1064-128">Questo parametro viene utilizzato per controllare quando il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema.</span><span class="sxs-lookup"><span data-stu-id="f1064-128">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="f1064-129">Questo parametro viene usato in combinazione con la <a href="dn335289(v=exchg.10).md">configurazione</a> per impedire che alcuni parametri di sistema vengano impostati dalle impostazioni predefinite della configurazione selezionata.</span><span class="sxs-lookup"><span data-stu-id="f1064-129">This parameter is used in conjunction with <a href="dn335289(v=exchg.10).md">Configuration</a> to prevent some system parameters from being set away from the selected configuration's defaults.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-132"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span><span class="sxs-lookup"><span data-stu-id="f1064-132"><a href="dn335291(v=exchg.10).md">EnableFileCache</a></span></span></td>
<td><span data-ttu-id="f1064-133">Abilitare l'uso della cache dei file del sistema operativo per tutti i file gestiti.</span><span class="sxs-lookup"><span data-stu-id="f1064-133">Enable the use of the OS file cache for all managed files.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-136"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span><span class="sxs-lookup"><span data-stu-id="f1064-136"><a href="dn335381(v=exchg.10).md">EnableViewCache</a></span></span></td>
<td><span data-ttu-id="f1064-137">Consente di utilizzare l'I/O di file mappato alla memoria per i file di database.</span><span class="sxs-lookup"><span data-stu-id="f1064-137">Enable the use of memory mapped file I/O for database files.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-140"><a href="dn335292(v=exchg.10).md">Per la maggior parte</a></span><span class="sxs-lookup"><span data-stu-id="f1064-140"><a href="dn335292(v=exchg.10).md">KeyMost</a></span></span></td>
<td><span data-ttu-id="f1064-141">Questo parametro di sola lettura indica la lunghezza massima consentita della chiave di indice che è possibile selezionare per le dimensioni correnti della pagina del database (come configurato da <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span><span class="sxs-lookup"><span data-stu-id="f1064-141">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-144"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span><span class="sxs-lookup"><span data-stu-id="f1064-144"><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></span></span></td>
<td><span data-ttu-id="f1064-145">Questo parametro fornisce la compatibilità con le versioni precedenti con le convenzioni di denominazione dei file delle versioni precedenti del motore di database.</span><span class="sxs-lookup"><span data-stu-id="f1064-145">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-148"><a href="dn335294(v=exchg.10).md">TableClass10Name</a></span></span></td>
<td><span data-ttu-id="f1064-149">Impostare il nome associato alla tabella Class 10.</span><span class="sxs-lookup"><span data-stu-id="f1064-149">Set the name associated with table class 10.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-152"><a href="dn335385(v=exchg.10).md">TableClass11Name</a></span></span></td>
<td><span data-ttu-id="f1064-153">Impostare il nome associato alla tabella Class 11.</span><span class="sxs-lookup"><span data-stu-id="f1064-153">Set the name associated with table class 11.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-156"><a href="dn335387(v=exchg.10).md">TableClass12Name</a></span></span></td>
<td><span data-ttu-id="f1064-157">Impostare il nome associato alla tabella Class 12.</span><span class="sxs-lookup"><span data-stu-id="f1064-157">Set the name associated with table class 12.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-160"><a href="dn335388(v=exchg.10).md">TableClass13Name</a></span></span></td>
<td><span data-ttu-id="f1064-161">Impostare il nome associato alla tabella Class 13.</span><span class="sxs-lookup"><span data-stu-id="f1064-161">Set the name associated with table class 13.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-164"><a href="dn335295(v=exchg.10).md">TableClass14Name</a></span></span></td>
<td><span data-ttu-id="f1064-165">Impostare il nome associato alla tabella Class 14.</span><span class="sxs-lookup"><span data-stu-id="f1064-165">Set the name associated with table class 14.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-168"><a href="dn335390(v=exchg.10).md">TableClass15Name</a></span></span></td>
<td><span data-ttu-id="f1064-169">Impostare il nome associato alla tabella Class 15.</span><span class="sxs-lookup"><span data-stu-id="f1064-169">Set the name associated with table class 15.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-172"><a href="dn335297(v=exchg.10).md">TableClass1Name</a></span></span></td>
<td><span data-ttu-id="f1064-173">Impostare il nome associato alla tabella Class 1.</span><span class="sxs-lookup"><span data-stu-id="f1064-173">Set the name associated with table class 1.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-176"><a href="dn335389(v=exchg.10).md">TableClass2Name</a></span></span></td>
<td><span data-ttu-id="f1064-177">Impostare il nome associato alla tabella Class 2.</span><span class="sxs-lookup"><span data-stu-id="f1064-177">Set the name associated with table class 2.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-180"><a href="dn335296(v=exchg.10).md">TableClass3Name</a></span></span></td>
<td><span data-ttu-id="f1064-181">Impostare il nome associato alla tabella Class 3.</span><span class="sxs-lookup"><span data-stu-id="f1064-181">Set the name associated with table class 3.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-184"><a href="dn335395(v=exchg.10).md">TableClass4Name</a></span></span></td>
<td><span data-ttu-id="f1064-185">Impostare il nome associato alla tabella classe 4.</span><span class="sxs-lookup"><span data-stu-id="f1064-185">Set the name associated with table class 4.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-188"><a href="dn335401(v=exchg.10).md">TableClass5Name</a></span></span></td>
<td><span data-ttu-id="f1064-189">Impostare il nome associato alla tabella Class 5.</span><span class="sxs-lookup"><span data-stu-id="f1064-189">Set the name associated with table class 5.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-192"><a href="dn335298(v=exchg.10).md">TableClass6Name</a></span></span></td>
<td><span data-ttu-id="f1064-193">Impostare il nome associato alla tabella Class 6.</span><span class="sxs-lookup"><span data-stu-id="f1064-193">Set the name associated with table class 6.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-196"><a href="dn335402(v=exchg.10).md">TableClass7Name</a></span></span></td>
<td><span data-ttu-id="f1064-197">Impostare il nome associato alla tabella Class 7.</span><span class="sxs-lookup"><span data-stu-id="f1064-197">Set the name associated with table class 7.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-200"><a href="dn335299(v=exchg.10).md">TableClass8Name</a></span></span></td>
<td><span data-ttu-id="f1064-201">Impostare il nome associato alla tabella Class 8.</span><span class="sxs-lookup"><span data-stu-id="f1064-201">Set the name associated with table class 8.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="f1064-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span><span class="sxs-lookup"><span data-stu-id="f1064-204"><a href="dn335404(v=exchg.10).md">TableClass9Name</a></span></span></td>
<td><span data-ttu-id="f1064-205">Impostare il nome associato alla tabella Class 9.</span><span class="sxs-lookup"><span data-stu-id="f1064-205">Set the name associated with table class 9.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f1064-206">Inizio</span><span class="sxs-lookup"><span data-stu-id="f1064-206">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="f1064-207">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1064-207">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f1064-208">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f1064-208">Reference</span></span>

[<span data-ttu-id="f1064-209">Classe VistaParam</span><span class="sxs-lookup"><span data-stu-id="f1064-209">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="f1064-210">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="f1064-210">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
