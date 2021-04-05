---
description: 'Altre informazioni su: membri JET_INDEXLIST'
title: Membri JET_INDEXLIST
TOCTitle: JET_INDEXLIST members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXLIST
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexlist_members(v=EXCHG.10)
ms:contentKeyID: 55103660
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d7800ef911366bad40b2d02ee60e23b5d138d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058088"
---
# <a name="jet_indexlist-members"></a>Membri JET_INDEXLIST

Includi membri protetti  
Includi membri ereditati  

Informazioni su una tabella temporanea contenente informazioni su tutti gli indici per una tabella specifica.

Il tipo di [JET_INDEXLIST](./jet-indexlist-class.md) espone i membri seguenti.

## <a name="constructors"></a>Costruttori

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335166(v=exchg.10).md">JET_INDEXLIST</a></td>
<td></td>
</tr>
</tbody>
</table>


Inizio

## <a name="properties"></a>Proprietà

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335125(v=exchg.10).md">columnidcColumn</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di colonne nella chiave di indice. La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335126(v=exchg.10).md">columnidcEntry</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di voci nell'indice. Questo valore non è corrente e viene aggiornato solo da &quot; API. JetComputeStats &quot; . La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335127(v=exchg.10).md">columnidcKey</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di chiavi univoche nell'indice. Questo valore non è corrente e viene aggiornato solo da &quot; API. JetComputeStats &quot; . La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335129(v=exchg.10).md">columnidcoltyp</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il tipo di colonna della colonna da indicizzare. La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335130(v=exchg.10).md">columnidcolumnid</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il ColumnID della colonna da indicizzare. La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335167(v=exchg.10).md">columnidcolumnname</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il grbit che si applicano alla colonna indicizzata. Vedere <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>. La colonna è di tipo <a href="hh577895(v=exchg.10).md">Text</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335168(v=exchg.10).md">columnidCp</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviata la tabella codici della colonna indicizzata. La colonna è di tipo <a href="hh577895(v=exchg.10).md">short</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335136(v=exchg.10).md">columnidcPage</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il numero di pagine nell'indice. Questo valore non è corrente e viene aggiornato solo da &quot; API. JetComputeStats &quot; . La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335169(v=exchg.10).md">columnidgrbitColumn</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il grbit che si applicano alla colonna indicizzata. Vedere <a href="hh579266(v=exchg.10).md">IndexKeyGrbit</a>. La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335134(v=exchg.10).md">columnidgrbitIndex</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il grbits usato nell'indice. Vedere <a href="hh578433(v=exchg.10).md">CreateIndexGrbit</a>. La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335170(v=exchg.10).md">columnidiColumn</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato l'indice di della colonna nella chiave di indice. La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335138(v=exchg.10).md">columnidindexname</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato il nome dell'indice. La colonna è di tipo <a href="hh577895(v=exchg.10).md">Text</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335171(v=exchg.10).md">columnidLangid</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui è archiviato l'ID lingua (LCID) dell'indice. La colonna è di tipo <a href="hh577895(v=exchg.10).md">short</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335172(v=exchg.10).md">columnidLCMapFlags</a></td>
<td>Ottiene l'ColumnID della colonna nella tabella temporanea in cui sono archiviati i flag di normalizzazione Unicode per l'indice. La colonna è di tipo <a href="hh577895(v=exchg.10).md">Long</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335173(v=exchg.10).md">cRecord</a></td>
<td>Ottiene il numero di record nella tabella temporanea.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335174(v=exchg.10).md">TableID</a></td>
<td>Ottiene TableID della tabella temporanea. Questa operazione deve essere chiusa quando la tabella non è più necessaria.</td>
</tr>
</tbody>
</table>


Inizio

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335165(v=exchg.10).md">ToString</a></td>
<td>Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn335123(v=exchg.10).md">JET_INDEXLIST</a>corrente. Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_INDEXLIST](./jet-indexlist-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
