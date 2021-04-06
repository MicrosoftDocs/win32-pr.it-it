---
description: 'Altre informazioni su: Proprietà JET_RETRIEVECOLUMN'
title: Proprietà JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2a42337e361fc7cbef60db70662ab7388c678903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758507"
---
# <a name="jet_retrievecolumn-properties"></a>Proprietà JET_RETRIEVECOLUMN

Includi membri protetti  
Includi membri ereditati  

Il tipo di [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) espone i membri seguenti.

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
<td>Ottiene la dimensione, in byte, dei dati recuperati da un'operazione di recupero colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335228(v=exchg.10).md">cbData</a></td>
<td>Ottiene o imposta le dimensioni in byte del buffer <a href="dn351040(v=exchg.10).md">pvData</a> . Tramite l'operazione di recupero colonna non vengono archiviati più dati in pvData rispetto a cbData.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335230(v=exchg.10).md">ColumnID</a></td>
<td>Ottiene o imposta l'identificatore di colonna per la colonna da recuperare.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></td>
<td>Ottiene l'ColumnID della colonna contrassegnata, multivalore o di tipo sparse quando tutte le colonne con tag vengono recuperate passando 0 come ColumnID.</td>
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
<td>Ottiene o imposta l'offset del primo byte da recuperare da una colonna di tipo <a href="hh577895(v=exchg.10).md">LongBinary</a> o <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351039(v=exchg.10).md">itagSequence</a></td>
<td>Ottiene o imposta il numero di sequenza dei valori contenuti in una colonna multivalore. Se itagSequence è 0, viene restituito il numero di istanze di una colonna multivalore anziché dati di colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351040(v=exchg.10).md">pvData</a></td>
<td>Ottiene o imposta il buffer in cui vengono archiviati i dati recuperati dalla colonna.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
