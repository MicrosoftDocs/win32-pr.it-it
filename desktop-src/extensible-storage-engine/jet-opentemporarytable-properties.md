---
description: 'Altre informazioni su: JET_OPENTEMPORARYTABLE proprietà'
title: JET_OPENTEMPORARYTABLE proprietà (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: JET_OPENTEMPORARYTABLE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_properties(v=EXCHG.10)
ms:contentKeyID: 55104127
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbba2937283ab9a3d008d3bad04329d1fd42b84e0de4a1a42e2e100d99a03854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016721"
---
# <a name="jet_opentemporarytable-properties"></a>JET_OPENTEMPORARYTABLE proprietà

Includere membri protetti  
Includere i membri ereditati  

Il [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) tipo espone i membri seguenti.

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
<td>Ottiene o imposta le dimensioni massime per una chiave che rappresenta una riga specificata. È possibile impostare le dimensioni massime della chiave per controllare la modalità di troncamento delle chiavi. Il troncamento delle chiavi è importante perché può influire su quando le righe vengono considerate distinte. Se questo parametro è impostato su 0 o 255, le dimensioni massime della chiave e la relativa semantica rimarranno identiche alle dimensioni massime della chiave supportate da Windows Server 2003. Questo parametro può anche essere impostato su un valore maggiore in funzione delle dimensioni della pagina del database per l'istanza <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. Per <a href="dn335292(v=exchg.10).md">altre informazioni, vedere KeyMost.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></td>
<td>Ottiene o imposta la quantità massima di dati che verranno utilizzati da qualsiasi colonna di lunghezza variabile per costruire una chiave per una determinata riga. Questo parametro può essere usato per controllare la quantità di spazio della chiave utilizzata da una determinata colonna chiave. Questo limite è in byte. Se questo parametro è zero o è uguale alla proprietà <a href="dn335290(v=exchg.10).md">cbKeyMost,</a> non è attivo alcun limite.</td>
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
<td>Ottiene o imposta l'ID delle impostazioni locali e i flag di normalizzazione da utilizzare per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. Quando questo parametro è Null, verrà usato l'LCID predefinito per confrontare le colonne chiave Unicode nella tabella temporanea. L'LCID predefinito è l'inglese degli Stati Uniti. Quando questo parametro è Null, verranno usati i flag di normalizzazione predefiniti per confrontare i dati delle colonne chiave Unicode nella tabella temporanea. I flag di normalizzazione predefiniti sono: NORM_IGNORECASE, NORM_IGNOREKANATYPE e NORM_IGNOREWIDTH.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">prgcolumndef</a></td>
<td>Ottiene o imposta le definizioni di colonna per le colonne create nella tabella temporanea.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">prgcolumnid</a></td>
<td>Ottiene o imposta il buffer di output che riceve la matrice di ID di colonna generati durante la creazione della tabella temporanea. Gli ID colonna in questa matrice corrispondono esattamente alla matrice di input delle definizioni di colonna. Di conseguenza, le dimensioni di questo buffer devono corrispondere alle dimensioni di <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">tableid</a></td>
<td>Ottiene l'handle di tabella per la tabella temporanea creata in seguito a una chiamata riuscita a JetOpenTemporaryTable.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_OPENTEMPORARYTABLE classe](./jet-opentemporarytable-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
