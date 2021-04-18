---
description: 'Altre informazioni su: membri JET_SETCOLUMN'
title: Membri JET_SETCOLUMN
TOCTitle: JET_SETCOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103848
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9c07f372705b20da09f2b3c3f1e5320771712c12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553757"
---
# <a name="jet_setcolumn-members"></a>Membri JET_SETCOLUMN

Includi membri protetti  
Includi membri ereditati  

Contiene i parametri di input e output per [JetSetColumns (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetsetcolumns-method.md). I campi della struttura descrivono il valore della colonna da impostare, come impostarlo e dove ottenere i dati del set di colonne.

Il tipo di [JET_SETCOLUMN](./jet-setcolumn-class.md) espone i membri seguenti.

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
<td><a href="dn335262(v=exchg.10).md">JET_SETCOLUMN</a></td>
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
<td><a href="dn335266(v=exchg.10).md">cbData</a></td>
<td>Ottiene o imposta la dimensione dei dati da impostare.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335268(v=exchg.10).md">ColumnID</a></td>
<td>Ottiene o imposta l'identificatore di colonna per una colonna da impostare.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335269(v=exchg.10).md">Err</a></td>
<td>Ottiene il codice di errore o l'avviso restituito dall'operazione set Column.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335270(v=exchg.10).md">grbit</a></td>
<td>Ottiene o imposta le opzioni per l'operazione set Column.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335271(v=exchg.10).md">ibData</a></td>
<td>Ottiene o imposta l'offset dei dati da impostare.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335272(v=exchg.10).md">ibLongValue</a></td>
<td>Ottiene o imposta l'offset al primo byte da impostare in una colonna di tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335273(v=exchg.10).md">itagSequence</a></td>
<td>Ottiene o imposta il numero di sequenza del valore in una colonna multivalore da impostare. La matrice di valori è in base uno. Il primo valore è Sequence 1, non 0 (zero). Se la colonna record ha un solo valore, è necessario passare 1 come itagSequence se tale valore viene sostituito. Il valore 0 (zero) indica di aggiungere una nuova istanza di valore di colonna alla fine della sequenza dei valori di colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351058(v=exchg.10).md">pvData</a></td>
<td>Ottiene o imposta un puntatore ai dati da impostare.</td>
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
<td><a href="dn351056(v=exchg.10).md">ContentEquals</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335264(v=exchg.10).md">DeepClone</a></td>
<td>Restituisce una copia completa dell'oggetto.</td>
</tr>
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
<td><a href="dn335265(v=exchg.10).md">ToString</a></td>
<td>Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a>corrente. Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_SETCOLUMN](./jet-setcolumn-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
