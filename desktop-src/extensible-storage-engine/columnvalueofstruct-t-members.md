---
description: 'Altre informazioni su: Membri <T> ColumnValueOfStruct'
title: Membri ColumnValueOfStruct(T)
TOCTitle: ColumnValueOfStruct(T) members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.ColumnValueOfStruct`1
ms:mtpsurl: https://msdn.microsoft.com/library/Dn334217(v=EXCHG.10)
ms:contentKeyID: 55101002
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 290a6180765992b23a386bb36ba4d5be85efaf1183875eeca0b02543bb1f1c08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042349"
---
# <a name="columnvalueofstructt-members"></a>Membri \<T\> columnValueOfStruct

Includere membri protetti  
Includi membri ereditati  

Impostare una colonna di un tipo struct ,ad esempio Int32/Guid.

Il [tipo ColumnValueOfStruct \<T\> ](./columnvalueofstruct-t-class.md) espone i membri seguenti.

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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn334175(v=exchg.10).md">ColumnValueOfStruct &lt; T&gt;</a></td>
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
<td><a href="dn334166(v=exchg.10).md">Id colonna</a></td>
<td>Ottiene o imposta l'elemento columnid da impostare o recuperare. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Error (Errore) (Error (Errore)e)</a></td>
<td>Ottiene l'avviso generato dal recupero o dall'impostazione di questa colonna. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Ottiene o imposta la sequenza itag della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334225(v=exchg.10).md">Length</a></td>
<td>Ottiene la lunghezza in byte di un valore di colonna, che è zero se column è Null, in caso contrario corrisponde a Size per questa colonna a dimensione fissa. Esegue l'override <a href="dn334213(v=exchg.10).md">di ColumnValue.Length.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Ottiene o imposta le opzioni di recupero delle colonne. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Ottiene o imposta le opzioni di aggiornamento delle colonne. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Proprietà protetta." alt="Protected property" /></td>
<td><a href="dn334172(v=exchg.10).md">Dimensioni</a></td>
<td>Ottiene le dimensioni del valore nella colonna. Viene restituito 0 per le colonne di dimensioni variabili, ad esempio binarie e stringa. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">Valore</a></td>
<td>Ottiene o imposta il valore nello struct.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334226(v=exchg.10).md">ValueAsObject</a></td>
<td>Ottiene l'ultimo valore impostato o recuperato della colonna. Il valore viene restituito come oggetto generico. Esegue l'override <a href="dn334214(v=exchg.10).md">di ColumnValue.ValueAsObject.</a></td>
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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn334178(v=exchg.10).md">CheckDataCount</a></td>
<td>Assicurarsi che i dati recuperati siano esattamente delle dimensioni necessarie per la struttura. In caso di mancata corrispondenza, viene generata un'eccezione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizza</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn334208(v=exchg.10).md">GetValueFromBytes</a></td>
<td>Dati recuperati da ESENT, decodificare i dati e impostare il valore nell'oggetto ColumnValue. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn334223(v=exchg.10).md">ToString</a></td>
<td>Ottiene una rappresentazione di stringa di questo oggetto . Esegue l'override <a href="dn334163(v=exchg.10).md">di ColumnValue.ToString().</a></td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe \<T\> ColumnValueOfStruct](./columnvalueofstruct-t-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
