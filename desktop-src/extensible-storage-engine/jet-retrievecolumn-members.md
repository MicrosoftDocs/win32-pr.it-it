---
description: 'Altre informazioni su: JET_RETRIEVECOLUMN membri'
title: JET_RETRIEVECOLUMN membri
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 84a778eb86c09da86f8c524daa321df9e8ca104122af6ecc13de88c2a824b79d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979481"
---
# <a name="jet_retrievecolumn-members"></a>JET_RETRIEVECOLUMN membri

Includere membri protetti  
Includere i membri ereditati  

Contiene i parametri di input e output [per JetRetrieveColumns(JET_SESID, \[ \] JET_TABLEID, , Int32)](./api.jetretrievecolumns-method.md). I campi nella struttura descrivono il valore della colonna da recuperare, come recuperarlo e dove salvare i risultati.

Il [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) tipo espone i membri seguenti.

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
<td><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></td>
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
<td><a href="dn335226(v=exchg.10).md">cbActual</a></td>
<td>Ottiene le dimensioni, in byte, dei dati recuperati da un'operazione di recupero della colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>Ottiene o imposta le dimensioni del buffer <a href="dn351040(v=exchg.10).md">pvData,</a> in byte. L'operazione di recupero della colonna non archivierà più dati in pvData rispetto a cbData.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">columnid</a></td>
<td>Ottiene o imposta l'identificatore di colonna per la colonna da recuperare.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></td>
<td>Ottiene il columnid della colonna con tag, multivalore o sparse quando tutte le colonne con tag vengono recuperate passando 0 come columnid.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335231(v=exchg.10).md">Err</a></td>
<td>Ottiene l'avviso restituito dal recupero della colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335232(v=exchg.10).md">grbit</a></td>
<td>Ottiene o imposta le opzioni per il recupero della colonna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335233(v=exchg.10).md">ibData</a></td>
<td>Ottiene o imposta l'offset nel buffer in cui verranno archiviati i dati.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335234(v=exchg.10).md">ibLongValue</a></td>
<td>Ottiene o imposta l'offset del primo byte da recuperare da una colonna di tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> <a href="hh577895(v=exchg.10).md">o LongText.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">itagSequence</a></td>
<td>Ottiene o imposta il numero di sequenza dei valori contenuti in una colonna multivalore. Se itagSequence è 0, viene restituito il numero di istanze di una colonna multivalore anziché i dati della colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">pvData</a></td>
<td>Ottiene o imposta il buffer che archivierà i dati recuperati dalla colonna.</td>
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
<td><a href="dn335224(v=exchg.10).md">ToString</a></td>
<td>Restituisce un <a href="/dotnet/api/system.string">oggetto String</a> che rappresenta l'oggetto <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>. Esegue l'override <a href="/dotnet/api/system.object.tostring#System_Object_ToString">di Object.ToString()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_RETRIEVECOLUMN classe](./jet-retrievecolumn-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
