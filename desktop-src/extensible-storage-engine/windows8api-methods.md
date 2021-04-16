---
description: 'Altre informazioni su: Metodi Windows8Api'
title: Metodi Windows8Api (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: Windows8Api methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api_methods(v=EXCHG.10)
ms:contentKeyID: 55104457
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d8eb8b822affcbf41c375f7ef23b6a71d03afc64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104550830"
---
# <a name="windows8api-methods"></a>Metodi Windows8Api

Includi membri protetti  
Includi membri ereditati  

Il tipo [Windows8Api](./windows8api-class.md) espone i membri seguenti.

## <a name="methods"></a>Metodi

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335374(v=exchg.10).md">JetBeginTransaction3</a></td>
<td>Consente a una sessione di immettere una transazione o di creare un nuovo punto di salvataggio in una transazione esistente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335489(v=exchg.10).md">JetCommitTransaction2</a></td>
<td>Esegue il commit delle modifiche apportate allo stato del database durante il punto di salvataggio corrente e ne esegue la migrazione al punto di salvataggio precedente. Se viene eseguito il commit del punto di salvataggio più esterno, verrà eseguito il commit delle modifiche apportate durante tale punto di salvataggio nello stato del database e la sessione uscirà dalla transazione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335488(v=exchg.10).md">JetCreateIndex4</a></td>
<td>Crea indici sui dati in un database ESE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335377(v=exchg.10).md">JetCreateTableColumnIndex4</a></td>
<td>Crea una tabella, aggiunge colonne e indici in tale tabella. <a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3 (JET_SESID, JET_DBID, JET_TABLECREATE)</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335493(v=exchg.10).md">JetGetErrorInfo</a></td>
<td>Ottiene informazioni estese su un errore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335378(v=exchg.10).md">JetOpenTemporaryTable2</a></td>
<td>Crea una tabella temporanea con un solo indice. Una tabella temporanea archivia e recupera i record esattamente come una tabella ordinaria creata con JetCreateTableColumnIndex. Tuttavia, le tabelle temporanee sono molto più veloci delle tabelle ordinarie a causa della loro natura volatile. Possono anche essere usati per ordinare ed eseguire molto rapidamente la rimozione dei duplicati nei set di record quando si accede in modo puramente sequenziale. Vedere anche <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, &quot; API. JetOpenTempTable2 &quot; , <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335382(v=exchg.10).md">JetPrereadIndexRanges</a></td>
<td>Se i record con gli intervalli di chiavi specificati non sono presenti nella cache buffer, avviare le letture asincrone per inserire i record nella cache buffer del database.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335496(v=exchg.10).md">JetResizeDatabase</a></td>
<td>Ridimensiona un database attualmente aperto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335383(v=exchg.10).md">JetSetCursorFilter</a></td>
<td>Impostare una matrice di filtri semplici per <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335495(v=exchg.10).md">JetSetSessionParameter</a></td>
<td>Imposta un parametro nello stato della sessione specificato, utilizzato per la durata della sessione o fino alla reimpostazione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335494(v=exchg.10).md">JetStopServiceInstance2</a></td>
<td>Prepara un'istanza per la chiusura. Può essere usato anche per riprendere un disattivazione precedente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335386(v=exchg.10).md">JetTryPrereadIndexRanges</a></td>
<td>Se i record con gli intervalli di chiavi specificati non sono presenti nella cache buffer, avviare le letture asincrone per inserire i record nella cache buffer del database.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335499(v=exchg.10).md">PrereadKeyRanges</a></td>
<td>Se i record con gli intervalli di chiavi specificati non sono presenti nella cache buffer, avviare le letture asincrone per inserire i record nella cache buffer del database.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Windows8Api](./windows8api-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
