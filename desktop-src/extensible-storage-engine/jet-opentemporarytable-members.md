---
description: 'Altre informazioni su: JET_OPENTEMPORARYTABLE membri'
title: JET_OPENTEMPORARYTABLE membri (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 934ea18663e2fd2de786bb44d32482f42fd45d38b9e6ec23e73caf815560b264
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560041"
---
# <a name="jet_opentemporarytable-members"></a>JET_OPENTEMPORARYTABLE membri

Includere membri protetti  
Includi membri ereditati  

Raccolta di parametri per il metodo JetOpenTemporaryTable.

Il [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) espone i membri seguenti.

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
<td><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></td>
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
<td><a href="dn335290(v=exchg.10).md">cbKeyMost</a></td>
<td>Ottiene o imposta la dimensione massima per una chiave che rappresenta una determinata riga. È possibile impostare le dimensioni massime delle chiavi per controllare la modalità di troncamento delle chiavi. Il troncamento delle chiavi è importante perché può influire sul momento in cui le righe vengono considerate distinte. Se questo parametro è impostato su 0 o 255, le dimensioni massime della chiave e la relativa semantica rimarranno identiche alle dimensioni massime della chiave supportate da Windows Server 2003. Questo parametro può anche essere impostato su un valore più grande come funzione delle dimensioni della pagina del database per l'istanza <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. Per <a href="dn335292(v=exchg.10).md">altre informazioni, vedere KeyMost.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></td>
<td>Ottiene o imposta la quantità massima di dati che verranno utilizzati da qualsiasi colonna a lunghezza variabile per costruire una chiave per una determinata riga. Questo parametro può essere usato per controllare la quantità di spazio della chiave utilizzato da una determinata colonna chiave. Questo limite è in byte. Se questo parametro è zero o è uguale alla <a href="dn335290(v=exchg.10).md">proprietà cbKeyMost,</a> non è attivo alcun limite.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335287(v=exchg.10).md">ccolumn</a></td>
<td>Ottiene o imposta il numero di colonne in <a href="dn351228(v=exchg.10).md">prgcolumndef.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351232(v=exchg.10).md">grbit</a></td>
<td>Ottiene o imposta le opzioni per la tabella temporanea.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335288(v=exchg.10).md">pidxunicode</a></td>
<td>Ottiene o imposta l'ID delle impostazioni locali e i flag di normalizzazione da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. Quando questo parametro è Null, verrà usato l'identificatore LCID predefinito per confrontare le colonne chiave Unicode nella tabella temporanea. L'LCID predefinito è la lingua inglese (Stati Uniti). Quando questo parametro è Null, verranno usati i flag di normalizzazione predefiniti per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">prgcolumndef</a></td>
<td>Ottiene o imposta le definizioni di colonna per le colonne create nella tabella temporanea.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">prgcolumnid</a></td>
<td>Ottiene o imposta il buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea. Gli ID di colonna in questa matrice corrisponderanno esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni di questo buffer devono corrispondere alle dimensioni di <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">tableid</a></td>
<td>Ottiene l'handle di tabella per la tabella temporanea creata in seguito a una chiamata riuscita a JetOpenTemporaryTable.</td>
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
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizza</a></td>
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
<td><a href="dn335286(v=exchg.10).md">ToString</a></td>
<td>Restituisce un <a href="/dotnet/api/system.string">oggetto String</a> che rappresenta l'oggetto <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>. Esegue l'override <a href="/dotnet/api/system.object.tostring#System_Object_ToString">di Object.ToString().</a></td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_OPENTEMPORARYTABLE classe](./jet-opentemporarytable-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
