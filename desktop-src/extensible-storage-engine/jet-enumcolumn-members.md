---
description: 'Altre informazioni su: JET_ENUMCOLUMN membri'
title: JET_ENUMCOLUMN membri
TOCTitle: JET_ENUMCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103614
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: a2a789b4a9793b9527a8b130671bf6948a58385973fd626b79a9ab6b59aa5128
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120116391"
---
# <a name="jet_enumcolumn-members"></a>JET_ENUMCOLUMN membri

Includere membri protetti  
Includere i membri ereditati  

Enumera i valori di colonna di un record usando la funzione JetEnumerateColumns. JetEnumerateColumns restituisce una matrice di JET_ENUMCOLUMNVALUE strutture. La matrice viene restituita in memoria allocata usando il callback fornito a tale funzione.

Il [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) tipo espone i membri seguenti.

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
<td><a href="dn335131(v=exchg.10).md">JET_ENUMCOLUMN</a></td>
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
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>Ottiene le dimensioni del valore enumerato per la colonna. Questo membro viene usato solo se <a href="dn335086(v=exchg.10).md">err</a> è uguale a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></td>
<td>Ottiene il numero di valori di colonna enumerati per la colonna. Questo membro viene usato solo se <a href="dn335086(v=exchg.10).md">err</a> non è <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">columnid</a></td>
<td>Ottiene l'ID columnid enumerato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">Err</a></td>
<td>Ottiene il codice di stato della colonna restituito dall'enumerazione .</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Ottiene il valore enumerato per la colonna. Questo membro viene usato solo se <a href="dn335086(v=exchg.10).md">err</a> è uguale a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>. Punta alla memoria allocata con il callback dell'allocatore <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> passato a <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>. Al termine, ricordarsi di rilasciare la memoria.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></td>
<td>Ottiene i valori di colonna enumerati per la colonna. Questo membro viene usato solo se <a href="dn335086(v=exchg.10).md">err</a> non è <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
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
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizzare</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335132(v=exchg.10).md">ToString</a></td>
<td>Restituisce un <a href="/dotnet/api/system.string">oggetto String</a> che rappresenta l'oggetto <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a>. Esegue l'override <a href="/dotnet/api/system.object.tostring#System_Object_ToString">di Object.ToString()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_ENUMCOLUMN classe](./jet-enumcolumn-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
