---
description: 'Altre informazioni su: campi VistaGrbits'
title: Campi VistaGrbits (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: VistaGrbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104318
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 3694dae8c55a5da838b8fcc058b369d7f0a59ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885774"
---
# <a name="vistagrbits-fields"></a><span data-ttu-id="8cec8-103">Campi VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="8cec8-103">VistaGrbits fields</span></span>

<span data-ttu-id="8cec8-104">Includi membri protetti</span><span class="sxs-lookup"><span data-stu-id="8cec8-104">Include protected members</span></span>  
<span data-ttu-id="8cec8-105">Includi membri ereditati</span><span class="sxs-lookup"><span data-stu-id="8cec8-105">Include inherited members</span></span>  

<span data-ttu-id="8cec8-106">Il tipo [VistaGrbits](./vistagrbits-class.md) espone i membri seguenti.</span><span class="sxs-lookup"><span data-stu-id="8cec8-106">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="8cec8-107">Campi</span><span class="sxs-lookup"><span data-stu-id="8cec8-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="8cec8-108">Nome</span><span class="sxs-lookup"><span data-stu-id="8cec8-108">Name</span></span></th>
<th><span data-ttu-id="8cec8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cec8-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="8cec8-112"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span><span class="sxs-lookup"><span data-stu-id="8cec8-112"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="8cec8-113">La sessione snapshot si ripete dopo JetOSSnapshotThaw e richiede una chiamata di funzione JetOSSnapshotEnd.</span><span class="sxs-lookup"><span data-stu-id="8cec8-113">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="8cec8-116"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span><span class="sxs-lookup"><span data-stu-id="8cec8-116"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="8cec8-117">Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave.</span><span class="sxs-lookup"><span data-stu-id="8cec8-117">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="8cec8-118">In caso contrario, l'indice avrebbe solo una voce per ogni multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice utilizzerebbe il primo multivalore da qualsiasi altra colonna chiave con colonne multivalore.</span><span class="sxs-lookup"><span data-stu-id="8cec8-118">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="8cec8-119">Se, ad esempio, si specifica questo flag per un indice sulla colonna A con i valori &quot; rosso &quot; e &quot; blu &quot; e sulla colonna B con i valori &quot; 1 &quot; e 2 &quot; , &quot; verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; rosso &quot; , &quot; 2 &quot; ; &quot; blu &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="8cec8-119">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="8cec8-120">In caso contrario, verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="8cec8-120">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="8cec8-123"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span><span class="sxs-lookup"><span data-stu-id="8cec8-123"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="8cec8-124">Se si specifica questo flag, eventuali aggiornamenti all'indice che comporteranno l'esito negativo di una chiave troncata verranno <a href="hh564840(v=exchg.10).md">troncati</a>.</span><span class="sxs-lookup"><span data-stu-id="8cec8-124">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="8cec8-125">In caso contrario, le chiavi verranno troncate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8cec8-125">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="8cec8-128"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span><span class="sxs-lookup"><span data-stu-id="8cec8-128"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="8cec8-129">Indice su più colonne multivalore, ma solo con valori dello stesso itagSequence.</span><span class="sxs-lookup"><span data-stu-id="8cec8-129">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="8cec8-132"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span><span class="sxs-lookup"><span data-stu-id="8cec8-132"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="8cec8-133">I log delle transazioni devono essere presenti nella directory del file di log, ad esempio non è possibile avviare automaticamente un nuovo flusso.</span><span class="sxs-lookup"><span data-stu-id="8cec8-133">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="8cec8-136"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span><span class="sxs-lookup"><span data-stu-id="8cec8-136"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="8cec8-137">Eseguire il ripristino, ma arrestare la fase di rollback.</span><span class="sxs-lookup"><span data-stu-id="8cec8-137">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="8cec8-138">Consente di eseguire la riproduzione dei log, quindi di eseguire la copia e la riproduzione di log aggiuntivi in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="8cec8-138">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="8cec8-141"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span><span class="sxs-lookup"><span data-stu-id="8cec8-141"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="8cec8-142">Impostazione predefinita per la voce della mappa di database non presente nella stessa posizione.</span><span class="sxs-lookup"><span data-stu-id="8cec8-142">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="8cec8-145"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span><span class="sxs-lookup"><span data-stu-id="8cec8-145"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="8cec8-146">Il motore può contrassegnare le intestazioni del database nel modo appropriato (ad esempio, un backup completo completato), anche se la chiamata a Truncate non è stata completata.</span><span class="sxs-lookup"><span data-stu-id="8cec8-146">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><span data-ttu-id="8cec8-149"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span><span class="sxs-lookup"><span data-stu-id="8cec8-149"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="8cec8-150">Al completamento del ripristino, troncare i file di log.</span><span class="sxs-lookup"><span data-stu-id="8cec8-150">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8cec8-151">Inizio</span><span class="sxs-lookup"><span data-stu-id="8cec8-151">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="8cec8-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8cec8-152">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8cec8-153">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8cec8-153">Reference</span></span>

[<span data-ttu-id="8cec8-154">Classe VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="8cec8-154">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="8cec8-155">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="8cec8-155">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
