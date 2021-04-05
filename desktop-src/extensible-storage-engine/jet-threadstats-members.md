---
description: 'Altre informazioni su: membri JET_THREADSTATS'
title: Membri di JET_THREADSTATS (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_THREADSTATS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats_members(v=EXCHG.10)
ms:contentKeyID: 39514028
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f8b824f716d35c3039bb77af745cf6cf08dfc9cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968168"
---
# <a name="jet_threadstats-members"></a>Membri JET_THREADSTATS

Includi membri protetti  
Includi membri ereditati  

Contiene statistiche cumulative sul lavoro eseguito dal motore di database sul thread corrente. Queste informazioni vengono restituite tramite JetGetThreadStats.

Il tipo di [JET_THREADSTATS](./jet-threadstats-structure2.md) espone i membri seguenti.

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
<td><a href="hh578305(v=exchg.10).md">cbLogRecord</a></td>
<td>Ottiene le dimensioni totali, in byte, dei record del log delle transazioni generate dal motore di database sul thread corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578110(v=exchg.10).md">cLogRecord</a></td>
<td>Ottiene il numero totale di record del log delle transazioni generati dal motore di database sul thread corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh578651(v=exchg.10).md">cPageDirtied</a></td>
<td>Ottiene il numero totale di pagine di database, senza modifiche non scritte, modificate dal motore di database sul thread corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh557376(v=exchg.10).md">cPagePreread</a></td>
<td>Ottiene il numero totale di pagine di database prelette dal disco dal motore di database sul thread corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh163392(v=exchg.10).md">cPageRead</a></td>
<td>Ottiene il numero totale di pagine del database recuperate dal disco dal motore di database sul thread corrente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh596234(v=exchg.10).md">cPageRedirtied</a></td>
<td>Ottiene il numero totale di pagine di database, con modifiche non scritte, modificate dal motore di database sul thread corrente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="hh557174(v=exchg.10).md">cPageReferenced</a></td>
<td>Ottiene il numero totale di pagine del database visitate dal motore di database sul thread corrente.</td>
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
<td><a href="hh565584(v=exchg.10).md">Aggiungere</a></td>
<td>Aggiungere le statistiche in due strutture di JET_THREADSTATS.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh538903(v=exchg.10).md">Creare</a></td>
<td>Crea una nuova struttura di <a href="hh578565(v=exchg.10).md">JET_THREADSTATS</a> con il valore specificato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="hh557146(v=exchg.10).md">Equals (oggetto)</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza. Esegue l'override di <a href="/dotnet/api/system.valuetype.equals#System_ValueType_Equals_System_Object_">ValueType. Equals (Object)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="hh596601(v=exchg.10).md">Uguale a (JET_THREADSTATS)</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="hh579156(v=exchg.10).md">GetHashCode</a></td>
<td>Restituisce il codice hash per l'istanza. Esegue l'override di <a href="/dotnet/api/system.valuetype.gethashcode#System_ValueType_GetHashCode">ValueType. GetHashCode ()</a>.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh579433(v=exchg.10).md">Sottrarre</a></td>
<td>Calcolare la differenza nelle statistiche tra due strutture di JET_THREADSTATS.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="hh558249(v=exchg.10).md">ToString</a></td>
<td>Ottiene una rappresentazione di stringa di questo oggetto. Esegue l'override di <a href="/dotnet/api/system.valuetype.tostring#System_ValueType_ToString">ValueType. ToString ()</a>.</td>
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
<td><a href="hh163281(v=exchg.10).md">Oltre</a></td>
<td>Aggiungere le statistiche in due strutture di JET_THREADSTATS.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh558521(v=exchg.10).md">Uguaglianza</a></td>
<td>Determina se due istanze specificate di JET_THREADSTATS sono uguali.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh577527(v=exchg.10).md">Disuguaglianza</a></td>
<td>Determina se due istanze specificate di JET_THREADSTATS non sono uguali.</td>
</tr>
<tr class="even">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operatore pubblico" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="hh557686(v=exchg.10).md">Sottrazione</a></td>
<td>Calcolare la differenza nelle statistiche tra due strutture di JET_THREADSTATS.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_THREADSTATS](./jet-threadstats-structure2.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
