---
description: 'Altre informazioni su: JET_COLUMNBASE membri'
title: 'Membri di JET_COLUMNBASE '
TOCTitle: JET_COLUMNBASE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase_members(v=EXCHG.10)
ms:contentKeyID: 55103414
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e47734e511f9acdd4f483dd5a9e28a1a3039bcd2a408f755d3e88cfb8cfd9836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781691"
---
# <a name="jet_columnbase-members"></a>Membri di JET_COLUMNBASE 

Includere membri protetti  
Includere i membri ereditati  

Descrive una colonna in una tabella di un database ESENT.

Il [JET_COLUMNBASE](./jet-columnbase-class.md) tipo espone i membri seguenti.

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
<td><a href="dn335065(v=exchg.10).md">cbMax</a></td>
<td>Ottiene la lunghezza massima della colonna. Ciò è significativo solo per le colonne di tipo <a href="hh577895(v=exchg.10).md">Text</a>, <a href="hh577895(v=exchg.10).md">LongText</a>, <a href="hh577895(v=exchg.10).md">Binary</a> <a href="hh577895(v=exchg.10).md">e LongBinary</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351019(v=exchg.10).md">coltyp</a></td>
<td>Ottiene il tipo della colonna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335024(v=exchg.10).md">columnid</a></td>
<td>Ottiene l'id colonna della colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335066(v=exchg.10).md">cp</a></td>
<td>Ottiene la tabella codici della colonna. Ciò è significativo solo per le colonne di tipo <a href="hh577895(v=exchg.10).md">Text</a> e <a href="hh577895(v=exchg.10).md">LongText.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351020(v=exchg.10).md">grbit</a></td>
<td>Ottiene le opzioni di colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335067(v=exchg.10).md">szBaseColumnName</a></td>
<td>Ottiene il nome della colonna nella tabella modello.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335026(v=exchg.10).md">szBaseTableName</a></td>
<td>Ottiene la tabella da cui la tabella corrente eredita il DDL.</td>
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
<td><a href="dn335062(v=exchg.10).md">Equals(Object)</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza. Esegue l'override <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">di Object.Equals(Object)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351009(v=exchg.10).md">Equals(JET_COLUMNBASE)</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizzare</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335023(v=exchg.10).md">GetHashCode</a></td>
<td>Restituisce il codice hash per l'istanza. Esegue l'override <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">di Object.GetHashCode()</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335064(v=exchg.10).md">ToString</a></td>
<td>Restituisce un <a href="/dotnet/api/system.string">oggetto String</a> che rappresenta l'oggetto <a href="dn335045(v=exchg.10).md">JET_COLUMNBASE</a>. Esegue l'override <a href="/dotnet/api/system.object.tostring#System_Object_ToString">di Object.ToString()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_COLUMNBASE classe](./jet-columnbase-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
