---
description: 'Altre informazioni su: Membri BytesColumnValue'
title: Membri bytesColumnValue
TOCTitle: BytesColumnValue members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.BytesColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue_members(v=EXCHG.10)
ms:contentKeyID: 55100914
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: b5c82031298f5cf1bee82e424401bb8994a414353c1ccd04cb8aa0fbb75ac557
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118084167"
---
# <a name="bytescolumnvalue-members"></a>Membri bytesColumnValue

Includere membri protetti  
Includere i membri ereditati  

Valore della colonna della matrice di byte.

Il [tipo BytesColumnValue](./bytescolumnvalue-class.md) espone i membri seguenti.

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
<td><a href="dn334168(v=exchg.10).md">BytesColumnValue</a></td>
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
<td><a href="dn334166(v=exchg.10).md">Columnid</a></td>
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
<td><a href="dn334126(v=exchg.10).md">Length</a></td>
<td>Ottiene la lunghezza in byte di un valore di colonna, ovvero zero se column è Null, in caso contrario corrisponde alla lunghezza effettiva della matrice di byte. Esegue l'override <a href="dn334213(v=exchg.10).md">di ColumnValue.Length.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Ottiene o imposta le opzioni di recupero della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Ottiene o imposta le opzioni di aggiornamento della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Proprietà protetta." alt="Protected property" /></td>
<td><a href="dn334176(v=exchg.10).md">Dimensioni</a></td>
<td>Ottiene le dimensioni del valore nella colonna. Viene restituito 0 per le colonne con dimensioni variabili, ad esempio binarie e stringa. Esegue l'override <a href="dn334172(v=exchg.10).md">di ColumnValue.Size.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334129(v=exchg.10).md">Valore</a></td>
<td>Ottiene o imposta il valore della colonna. Usare <a href="dn334138(v=exchg.10).md">SetColumns(JET_SESID, JET_TABLEID, [])</a> per aggiornare un record con il valore della colonna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334177(v=exchg.10).md">Oggetto ValueAsObject</a></td>
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
<td><a href="dn334173(v=exchg.10).md">GetValueFromBytes</a></td>
<td>Dati recuperati da ESENT, decodificare i dati e impostare il valore nell'oggetto ColumnValue. (Esegue <a href="dn334208(v=exchg.10).md">l'override di ColumnValue.GetValueFromBytes([], Int32, Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn334124(v=exchg.10).md">ToString</a></td>
<td>Restituisce un <a href="/dotnet/api/system.string">oggetto String</a> che rappresenta l'oggetto <a href="dn334170(v=exchg.10).md">BytesColumnValue corrente.</a> Esegue l'override <a href="dn334163(v=exchg.10).md">di ColumnValue.ToString()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe BytesColumnValue](./bytescolumnvalue-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
