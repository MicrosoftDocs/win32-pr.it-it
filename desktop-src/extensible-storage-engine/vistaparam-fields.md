---
description: 'Altre informazioni su: Campi VistaParam'
title: Campi VistaParam (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: VistaParam fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaParam
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam_fields(v=EXCHG.10)
ms:contentKeyID: 55104336
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 3684f6d50ba0ca107614276776e375bc90b32a0d0e3e0112dded07b6e9e5bcdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119718851"
---
# <a name="vistaparam-fields"></a>Campi VistaParam

Includere membri protetti  
Includi membri ereditati  

Il [tipo VistaParam](./vistaparam-class.md) espone i membri seguenti.

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
<td><a href="dn335379(v=exchg.10).md">CachedClosedTables</a></td>
<td>Questo parametro controlla il numero di risorse albero B+ memorizzate nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione. Valori di grandi dimensioni per questo parametro causeranno l'uso di una quantità maggiore di memoria da parte del motore di database, ma aumenterà la velocità con cui un numero elevato di tabelle può essere aperto in modo casuale dall'applicazione. Ciò è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335289(v=exchg.10).md">Configuration</a></td>
<td>Questo parametro espone più set di valori predefiniti per l'intero set di parametri di sistema. Quando questo parametro è impostato su una configurazione specifica, tutti i valori dei parametri di sistema vengono reimpostati sui valori predefiniti per tale configurazione. Se la configurazione è impostata per un'istanza specifica, i parametri di sistema globali non verranno reimpostati sui valori predefiniti. Configurazione piccola (0): il motore di database è ottimizzato per l'uso della memoria. Configurazione legacy (1): il motore di database ha le impostazioni predefinite tradizionali.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335380(v=exchg.10).md">EnableAdvanced</a></td>
<td>Questo parametro viene utilizzato per controllare quando il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema. Questo parametro viene usato insieme a <a href="dn335289(v=exchg.10).md">Configuration per</a> impedire che alcuni parametri di sistema vengano impostati in base alle impostazioni predefinite della configurazione selezionata.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335291(v=exchg.10).md">EnableFileCache</a></td>
<td>Abilitare l'uso della cache dei file del sistema operativo per tutti i file gestiti.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335381(v=exchg.10).md">EnableViewCache</a></td>
<td>Abilitare l'uso di I/O di file mappati alla memoria per i file di database.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335292(v=exchg.10).md">KeyMost</a></td>
<td>Questo parametro di sola lettura indica la lunghezza massima consentita per la chiave di indice che può essere selezionata per le dimensioni di pagina correnti del database (come configurato da <a href="hh596135(v=exchg.10).md">DatabasePageSize).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335384(v=exchg.10).md">LegacyFileNames</a></td>
<td>Questo parametro garantisce la compatibilità con le versioni precedenti delle convenzioni di denominazione dei file delle versioni precedenti del motore di database.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335294(v=exchg.10).md">TableClass10Name</a></td>
<td>Impostare il nome associato alla classe di tabella 10.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335385(v=exchg.10).md">TableClass11Name</a></td>
<td>Impostare il nome associato alla classe di tabella 11.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335387(v=exchg.10).md">TableClass12Name</a></td>
<td>Impostare il nome associato alla classe di tabella 12.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335388(v=exchg.10).md">TableClass13Name</a></td>
<td>Impostare il nome associato alla classe di tabella 13.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335295(v=exchg.10).md">TableClass14Name</a></td>
<td>Impostare il nome associato alla classe di tabella 14.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335390(v=exchg.10).md">TableClass15Name</a></td>
<td>Impostare il nome associato alla classe di tabella 15.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335297(v=exchg.10).md">TableClass1Name</a></td>
<td>Impostare il nome associato alla classe di tabella 1.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335389(v=exchg.10).md">TableClass2Name</a></td>
<td>Impostare il nome associato alla classe di tabella 2.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335296(v=exchg.10).md">TableClass3Name</a></td>
<td>Impostare il nome associato alla classe di tabella 3.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335395(v=exchg.10).md">TableClass4Name</a></td>
<td>Impostare il nome associato alla classe di tabella 4.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335401(v=exchg.10).md">TableClass5Name</a></td>
<td>Impostare il nome associato alla classe di tabella 5.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335298(v=exchg.10).md">TableClass6Name</a></td>
<td>Impostare il nome associato alla classe di tabella 6.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335402(v=exchg.10).md">TableClass7Name</a></td>
<td>Impostare il nome associato alla classe di tabella 7.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335299(v=exchg.10).md">TableClass8Name</a></td>
<td>Impostare il nome associato alla classe di tabella 8.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn335404(v=exchg.10).md">TableClass9Name</a></td>
<td>Impostare il nome associato alla classe di tabella 9.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe VistaParam](./vistaparam-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
