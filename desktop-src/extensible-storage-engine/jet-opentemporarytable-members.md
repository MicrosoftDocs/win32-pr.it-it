---
description: 'Altre informazioni su: membri JET_OPENTEMPORARYTABLE'
title: Membri di JET_OPENTEMPORARYTABLE (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af149ecba6858aca4b4877fc9446872386406838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104557860"
---
# <a name="jet_opentemporarytable-members"></a>Membri JET_OPENTEMPORARYTABLE

Includi membri protetti  
Includi membri ereditati  

Raccolta di parametri per il metodo JetOpenTemporaryTable.

Il tipo di [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) espone i membri seguenti.

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
<td>Ottiene o imposta la dimensione massima per una chiave che rappresenta una determinata riga. È possibile impostare la dimensione massima della chiave per controllare la modalità di troncamento delle chiavi. Il troncamento della chiave è importante perché può influire sul fatto che le righe siano considerate distinte. Se questo parametro è impostato su 0 o 255, le dimensioni massime della chiave e la relativa semantica rimarranno identiche alle dimensioni massime della chiave supportate da Windows Server 2003. Questo parametro può essere impostato anche su un valore maggiore come funzione delle dimensioni della pagina del database per l'istanza <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. Per <a href="dn335292(v=exchg.10).md">ulteriori</a> informazioni, vedere.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></td>
<td>Ottiene o imposta la quantità massima di dati che verranno utilizzati da qualsiasi variabile lengthcolumn per costruire una chiave per una determinata riga. Questo parametro può essere utilizzato per controllare la quantità di spazio chiave utilizzata da una determinata colonna chiave. Questo limite è in byte. Se questo parametro è zero o è uguale alla proprietà <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , non è attivo alcun limite.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335287(v=exchg.10).md">CColumn</a></td>
<td>Ottiene o imposta il numero di colonne in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351232(v=exchg.10).md">grbit</a></td>
<td>Ottiene o imposta le opzioni per la tabella temporanea.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335288(v=exchg.10).md">pidxunicode</a></td>
<td>Ottiene o imposta l'ID delle impostazioni locali e i flag di normalizzazione da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. Se questo parametro è null, verrà utilizzato il valore LCID predefinito per confrontare eventuali colonne chiave Unicode nella tabella temporanea. Il valore LCID predefinito corrisponde alle impostazioni locali per l'inglese (Stati Uniti). Se questo parametro è null, i flag di normalizzazione predefiniti verranno utilizzati per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">prgcolumndef</a></td>
<td>Ottiene o imposta le definizioni di colonna per le colonne create nella tabella temporanea.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">prgcolumnid</a></td>
<td>Ottiene o imposta il buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea. Gli ID di colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni del buffer devono corrispondere alla dimensione di <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">TableID</a></td>
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
<td><a href="dn335286(v=exchg.10).md">ToString</a></td>
<td>Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta la <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>corrente. Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
