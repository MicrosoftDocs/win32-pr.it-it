---
description: 'Altre informazioni su: Proprietà JET_INDEXCREATE'
title: Proprietà JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968347"
---
# <a name="jet_indexcreate-properties"></a>Proprietà JET_INDEXCREATE

Includi membri protetti  
Includi membri ereditati  

Il tipo di [JET_INDEXCREATE](./jet-indexcreate-class.md) espone i membri seguenti.

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
<td><a href="dn335122(v=exchg.10).md">cbKey</a></td>
<td>Ottiene o imposta la lunghezza, in caratteri, di szKey, inclusi i due valori null di terminazione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">cbKeyMost</a></td>
<td>Ottiene o imposta la dimensione massima consentita, in byte, per le chiavi nell'indice. Le dimensioni minime massime supportate per la chiave sono JET_cbKeyMostMin (255), ovvero le dimensioni massime della chiave legacy. Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. È possibile recuperare le dimensioni massime della <a href="dn351156(v=exchg.10).md">chiave con la</a>chiave. Questo parametro viene ignorato in Windows XP e Windows Server 2003. A differenza dell'API non gestita, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) non è necessario, verrà aggiunto automaticamente.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></td>
<td>Ottiene o imposta la lunghezza massima, in byte, di ogni colonna da archiviare nell'indice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></td>
<td>Ottiene o imposta il numero di colonne condizionali.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335157(v=exchg.10).md">Err</a></td>
<td>Ottiene o imposta il codice di errore della creazione di questo indice.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">grbit</a></td>
<td>Ottiene o imposta le opzioni di creazione degli indici.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">pidxUnicode</a></td>
<td>Ottiene o imposta le opzioni di confronto Unicode facoltative.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pSpaceHints</a></td>
<td>Ottiene o imposta gli hint per l'allocazione, la manutenzione e l'utilizzo dello spazio.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></td>
<td>Ottiene o imposta le colonne condizionali facoltative.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335121(v=exchg.10).md">szIndexName</a></td>
<td>Ottiene o imposta il nome dell'indice da creare.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335161(v=exchg.10).md">szKey</a></td>
<td>Ottiene o imposta la descrizione della chiave di indice. Si tratta di una stringa doppia con terminazione null di token delimitati da null. Ogni token è nel formato [direction-specifier] [column-name], dove Direction-Specification è &quot; + &quot; o &quot; - &quot; . ad esempio, un szKey di &quot; + abc\0-def\0 + ghi\0 &quot; indurrà l'indice sulle tre colonne &quot; ABC &quot; (in ordine crescente), &quot; def &quot; (in ordine decrescente) e &quot; ghi &quot; (in ordine crescente).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">ulDensity</a></td>
<td>Ottiene o imposta la densità dell'indice.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_INDEXCREATE](./jet-indexcreate-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
