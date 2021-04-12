---
description: 'Altre informazioni su: membri JET_COLUMNBASE'
title: 'Membri di JET_COLUMNBASE '
TOCTitle: JET_COLUMNBASE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase_members(v=EXCHG.10)
ms:contentKeyID: 55103414
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 72f26e02963d1cc0617fb908ce325c0c0099f7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348286"
---
# <a name="jet_columnbase-members"></a>Membri di JET_COLUMNBASE 

Includi membri protetti  
Includi membri ereditati  

Descrive una colonna in una tabella di un database ESENT.

Il tipo di [JET_COLUMNBASE](./jet-columnbase-class.md) espone i membri seguenti.

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
<td>Ottiene la lunghezza massima della colonna. Questa operazione è significativa solo per le colonne di tipo <a href="hh577895(v=exchg.10).md">Text</a>, <a href="hh577895(v=exchg.10).md">LONGTEXT</a>, <a href="hh577895(v=exchg.10).md">Binary</a> e <a href="hh577895(v=exchg.10).md">LongBinary</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351019(v=exchg.10).md">coltyp</a></td>
<td>Ottiene il tipo della colonna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335024(v=exchg.10).md">ColumnID</a></td>
<td>Ottiene l'ColumnID della colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335066(v=exchg.10).md">cp</a></td>
<td>Ottiene la tabella codici della colonna. Questa operazione è significativa solo per le colonne di tipo <a href="hh577895(v=exchg.10).md">Text</a> e <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351020(v=exchg.10).md">grbit</a></td>
<td>Ottiene le opzioni della colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335067(v=exchg.10).md">szBaseColumnName</a></td>
<td>Ottiene il nome della colonna nella tabella del modello.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335026(v=exchg.10).md">szBaseTableName</a></td>
<td>Ottiene la tabella da cui la tabella corrente eredita la DDL.</td>
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
<td><a href="dn335062(v=exchg.10).md">Equals (oggetto)</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza. Esegue l'override di <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object. Equals (Object)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351009(v=exchg.10).md">Uguale a (JET_COLUMNBASE)</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335023(v=exchg.10).md">GetHashCode</a></td>
<td>Restituisce il codice hash per l'istanza. Esegue l'override di <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object. GetHashCode ()</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335064(v=exchg.10).md">ToString</a></td>
<td>Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn335045(v=exchg.10).md">JET_COLUMNBASE</a>corrente. Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_COLUMNBASE](./jet-columnbase-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
