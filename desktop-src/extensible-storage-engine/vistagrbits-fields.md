---
description: 'Altre informazioni su: Campi VistaGrbits'
title: Campi VistaGrbits (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: VistaGrbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104318
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d81a176d04911f2c76767838a62e5202f9e80c059112c703a3673644fddb76f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967571"
---
# <a name="vistagrbits-fields"></a>Campi VistaGrbits

Includere membri protetti  
Includi membri ereditati  

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
<td>La sessione snapshot continua dopo JetOSSnapshotThaw e richiederà una chiamata di funzione JetOSSnapshotEnd.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></td>
<td>Se si specifica questo flag per un indice con più di una colonna chiave che è una colonna multivalore, verrà creata una voce di indice per ogni risultato di un prodotto incrociato di tutti i valori in tali colonne chiave. In caso contrario, l'indice avrebbe una sola voce per ogni multivalore nella colonna chiave più significativa che è una colonna multivalore e ognuna di queste voci di indice userebbe il primo multivalore di qualsiasi altra colonna chiave che sono colonne multivalore. Ad esempio, se è stato specificato questo flag per un indice sulla colonna A con i valori rosso e blu e sulla colonna B con i valori 1 e 2, verranno create le voci di indice &quot; &quot; &quot; &quot; &quot; &quot; &quot; &quot; seguenti: &quot; rosso , &quot; &quot; 1 &quot; ; &quot; rosso &quot; , &quot; 2 &quot; ; &quot; blu &quot; , &quot; 1 &quot; ; &quot; blu &quot; , &quot; 2 &quot; . In caso contrario, verranno create le voci di indice seguenti: &quot; rosso &quot; , &quot; 1 &quot; ; &quot; blu, &quot; &quot; 1 &quot; .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></td>
<td>Se si specifica questo flag, qualsiasi aggiornamento dell'indice che causerebbe l'esito negativo di una chiave troncata con <a href="hh564840(v=exchg.10).md">KeyTruncated.</a> In caso contrario, le chiavi verranno troncate automaticamente.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></td>
<td>Indicizzare più colonne multivalore, ma solo con valori della stessa itagSequence.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></td>
<td>I log delle transazioni devono essere presenti nella directory dei file di log, ovvero non è possibile avviare automaticamente un nuovo flusso.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></td>
<td>Eseguire il ripristino, ma interrompersi in fase di annullamento. Consente la riproduzione dei log presenti, quindi è possibile copiare e riprodurre log aggiuntivi in un secondo momento.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></td>
<td>Voce della mappa di database mancante per impostazione predefinita nella stessa posizione.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">TruncateDone</a></td>
<td>Il motore può contrassegnare le intestazioni del database come appropriato (ad esempio, un backup completo completato), anche se la chiamata a truncate non è stata completata.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></td>
<td>In caso di esito positivo del ripristino ammoramento, troncare i file di log.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe VistaGrbits](./vistagrbits-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
