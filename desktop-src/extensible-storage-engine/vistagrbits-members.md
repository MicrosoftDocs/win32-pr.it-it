---
description: 'Altre informazioni su: Membri di VistaGrbits'
title: Membri di VistaGrbits (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: VistaGrbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_members(v=EXCHG.10)
ms:contentKeyID: 55104213
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: be9908627d4351ec710fa6b1791d24779ab501b8e61bb342d96a3a0ec4afa87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978161"
---
# <a name="vistagrbits-members"></a>Membri di VistaGrbits

Includere membri protetti  
Includere i membri ereditati  

Grbit aggiunti alla versione Vista di ESENT.

Il [tipo VistaGrbits](./vistagrbits-class.md) espone i membri seguenti.

## <a name="fields"></a>Campi

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></td>
<td>La sessione snapshot continua dopo JetOSSnapshotThaw e richiede una chiamata di funzione JetOSSnapshotEnd.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></td>
<td>Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave. In caso contrario, l'indice avrebbe una sola voce per ogni multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice userebbe il primo multivalore da qualsiasi altra colonna chiave che sono colonne multivalore. Se ad esempio è stato specificato questo flag per un indice sulla colonna A con i valori rosso e blu e sulla colonna B con i valori 1 e 2, verranno create le voci di indice &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; seguenti: &quot; red , &quot; &quot; 1 &quot; ; &quot; rosso &quot; , &quot; 2 &quot; ; &quot; blu &quot; , &quot; 1 &quot; ; &quot; blu, &quot; &quot; 2 &quot; . In caso contrario, verranno create le voci di indice seguenti: &quot; red &quot; , &quot; 1 &quot; ; &quot; blu, &quot; &quot; 1 &quot; .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></td>
<td>Se si specifica questo flag, qualsiasi aggiornamento all'indice che causerebbe l'esito negativo di una chiave troncata con <a href="hh564840(v=exchg.10).md">KeyTruncated</a>. In caso contrario, le chiavi verranno troncate automaticamente.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></td>
<td>Indice su più colonne multivalore, ma solo con valori della stessa itagSequence.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></td>
<td>I log delle transazioni devono essere presenti nella directory del file di log, ad esempio non è possibile avviare automaticamente un nuovo flusso.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></td>
<td>Eseguire il ripristino, ma arrestarsi nella fase di annullamento. Consente la riproduzione dei log presenti, quindi in un secondo momento è possibile copiare e riprodurre altri log.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></td>
<td>La voce della mappa di database mancante viene per impostazione predefinita nella stessa posizione.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">TruncateDone</a></td>
<td>Il motore può contrassegnare le intestazioni del database come appropriate (ad esempio, un backup completo completato), anche se la chiamata a truncate non è stata completata.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></td>
<td>In caso di ripristino soft riuscito, troncare i file di log.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe VistaGrbits](./vistagrbits-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
