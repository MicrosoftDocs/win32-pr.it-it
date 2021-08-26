---
description: 'Altre informazioni su: JET_RECSIZE membri'
title: JET_RECSIZE membri (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_RECSIZE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_members(v=EXCHG.10)
ms:contentKeyID: 39510137
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8a39bc4aee3b033b735d5c4ebe818d189c36b1908ba8364200c4cb94b15459cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063751"
---
# <a name="jet_recsize-members"></a>JET_RECSIZE membri

Includere membri protetti  
Includere i membri ereditati  

Usato da [JetGetRecordSize(JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) per restituire informazioni sui requisiti di utilizzo di un record nello spazio dati utente, sul numero di colonne del set, sul numero di valori e sullo spazio di sovraccarico della struttura dei record ESENT.

Il [JET_RECSIZE](./jet-recsize-structure2.md) tipo espone i membri seguenti.

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
<td><a href="hh557581(v=exchg.10).md">cbData</a></td>
<td>Ottiene il set di dati utente nel record.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></td>
<td>Ottiene le dimensioni compresse dei dati utente nel record. È uguale a <a href="hh557581(v=exchg.10).md">cbData</a> se non vengono compressi valori long intrinseci.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh557913(v=exchg.10).md">cbLongValueData</a></td>
<td>Ottiene il set di dati utente nel record, ma archiviato nell'albero a valori lunghi.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></td>
<td>Ottiene le dimensioni compresse dei dati utente nell'albero a valori lunghi. È uguale a <a href="hh557913(v=exchg.10).md">cbLongValueData</a> se non vengono compressi valori long separati.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></td>
<td>Ottiene il sovraccarico dei dati di valore long.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh565836(v=exchg.10).md">cbOverhead</a></td>
<td>Ottiene il sovraccarico della struttura di record ESENT per questo record. Sono incluse le dimensioni della chiave del record.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></td>
<td>Ottiene il numero totale di colonne nel record compresse.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh596288(v=exchg.10).md">cLongValues</a></td>
<td>Ottiene il numero totale di valori long archiviati nell'albero dei valori long per questo record. Non sono inclusi valori long intrinseci.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh577486(v=exchg.10).md">cMultiValues</a></td>
<td>Ottiene l'accumulo del numero totale di valori oltre la prima per tutte le colonne del record.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></td>
<td>Ottiene il numero totale di colonne fisse e variabili impostate in questo record.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></td>
<td>Ottiene il numero totale di colonne contrassegnate impostate in questo record.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh538879(v=exchg.10).md">Aggiungere</a></td>
<td>Aggiungere le dimensioni in due JET_RECSIZE struttura.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="hh558506(v=exchg.10).md">Equals(Object)</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza. Esegue l'override <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">di ValueType.Equals(Object)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="hh577992(v=exchg.10).md">Equals(JET_RECSIZE)</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizzare</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="hh557078(v=exchg.10).md">GetHashCode</a></td>
<td>Restituisce il codice hash per l'istanza. Esegue l'override <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">di ValueType.GetHashCode()</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh579561(v=exchg.10).md">Sottrarre</a></td>
<td>Calcolare la differenza di dimensioni tra due JET_RECSIZE struttura.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ToString</a></td>
<td>Ereditato da <a href="/dotnet/api/system.valuetype">ValueType.</a></td>
</tr>
</tbody>
</table>


Inizio

## <a name="operators"></a>Operatori

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
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh578675(v=exchg.10).md">Addizione</a></td>
<td>Aggiungere le dimensioni in due JET_RECSIZE struttura.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh596362(v=exchg.10).md">Uguaglianza</a></td>
<td>Determina se due istanze specificate di JET_RECSIZE sono uguali.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh578809(v=exchg.10).md">Disuguaglianza</a></td>
<td>Determina se due istanze specificate di JET_RECSIZE non sono uguali.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh596696(v=exchg.10).md">Sottrazione</a></td>
<td>Calcolare la differenza di dimensioni tra due JET_RECSIZE struttura .</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_RECSIZE struttura](./jet-recsize-structure2.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
