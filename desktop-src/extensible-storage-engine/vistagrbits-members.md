---
description: 'Altre informazioni su: membri di VistaGrbits'
title: Membri di VistaGrbits (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 56145954b504f086ff36fbe84ea26768b8e3636a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104566963"
---
# <a name="vistagrbits-members"></a><span data-ttu-id="e6d80-103">Membri di VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="e6d80-103">VistaGrbits members</span></span>

<span data-ttu-id="e6d80-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="e6d80-104">Include protected members</span></span>  
<span data-ttu-id="e6d80-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="e6d80-105">Include inherited members</span></span>  

<span data-ttu-id="e6d80-106">Grbits che sono stati aggiunti alla versione vista di ESENT.</span><span class="sxs-lookup"><span data-stu-id="e6d80-106">Grbits that have been added to the Vista version of ESENT.</span></span>

<span data-ttu-id="e6d80-107">Il tipo [VistaGrbits](./vistagrbits-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="e6d80-107">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="e6d80-108">Campi</span><span class="sxs-lookup"><span data-stu-id="e6d80-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="e6d80-109">Nome</span><span class="sxs-lookup"><span data-stu-id="e6d80-109">Name</span></span></th>
<th><span data-ttu-id="e6d80-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6d80-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="e6d80-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span><span class="sxs-lookup"><span data-stu-id="e6d80-113"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="e6d80-114">La sessione snapshot si ripete dopo JetOSSnapshotThaw e richiede una chiamata di funzione JetOSSnapshotEnd.</span><span class="sxs-lookup"><span data-stu-id="e6d80-114">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="e6d80-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span><span class="sxs-lookup"><span data-stu-id="e6d80-117"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="e6d80-118">Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave.</span><span class="sxs-lookup"><span data-stu-id="e6d80-118">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="e6d80-119">In caso contrario, l'indice avrebbe solo una voce per ogni multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice utilizzerebbe il primo multivalore da qualsiasi altra colonna chiave con colonne multivalore.</span><span class="sxs-lookup"><span data-stu-id="e6d80-119">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="e6d80-120">Se, ad esempio, si specifica questo flag per un indice sulla colonna A con i valori &quot; rosso &quot; e &quot; blu &quot; e sulla colonna B con i valori &quot; 1 &quot; e 2 &quot; , &quot; verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; rosso &quot; , &quot; 2 &quot; ; &quot; blu &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="e6d80-120">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="e6d80-121">In caso contrario, verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="e6d80-121">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="e6d80-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span><span class="sxs-lookup"><span data-stu-id="e6d80-124"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="e6d80-125">Se si specifica questo flag, eventuali aggiornamenti all'indice che comporteranno l'esito negativo di una chiave troncata verranno <a href="hh564840(v=exchg.10).md">troncati</a>.</span><span class="sxs-lookup"><span data-stu-id="e6d80-125">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="e6d80-126">In caso contrario, le chiavi verranno troncate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e6d80-126">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="e6d80-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span><span class="sxs-lookup"><span data-stu-id="e6d80-129"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="e6d80-130">Indice su più colonne multivalore, ma solo con valori dello stesso itagSequence.</span><span class="sxs-lookup"><span data-stu-id="e6d80-130">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="e6d80-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span><span class="sxs-lookup"><span data-stu-id="e6d80-133"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="e6d80-134">I log delle transazioni devono essere presenti nella directory del file di log, ad esempio non è possibile avviare automaticamente un nuovo flusso.</span><span class="sxs-lookup"><span data-stu-id="e6d80-134">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="e6d80-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span><span class="sxs-lookup"><span data-stu-id="e6d80-137"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="e6d80-138">Eseguire il ripristino, ma arrestare la fase di rollback.</span><span class="sxs-lookup"><span data-stu-id="e6d80-138">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="e6d80-139">Consente di eseguire la riproduzione dei log, quindi di eseguire la copia e la riproduzione di log aggiuntivi in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="e6d80-139">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="e6d80-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span><span class="sxs-lookup"><span data-stu-id="e6d80-142"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="e6d80-143">Impostazione predefinita per la voce della mappa di database non presente nella stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="e6d80-143">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="e6d80-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span><span class="sxs-lookup"><span data-stu-id="e6d80-146"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="e6d80-147">Il motore può contrassegnare le intestazioni del database nel modo appropriato (ad esempio, un backup completo completato), anche se la chiamata a Truncate non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e6d80-147">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="e6d80-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span><span class="sxs-lookup"><span data-stu-id="e6d80-150"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="e6d80-151">Al completamento del ripristino, troncare i file di log.</span><span class="sxs-lookup"><span data-stu-id="e6d80-151">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e6d80-152">Inizio</span><span class="sxs-lookup"><span data-stu-id="e6d80-152">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="e6d80-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6d80-153">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6d80-154">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e6d80-154">Reference</span></span>

[<span data-ttu-id="e6d80-155">Classe VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="e6d80-155">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="e6d80-156">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="e6d80-156">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
