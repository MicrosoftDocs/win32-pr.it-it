---
description: 'Altre informazioni su: JET_ENUMCOLUMNID proprietà'
title: JET_ENUMCOLUMNID proprietà
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2abb02a5052747be5d3bf9f3f968e8ca2dfc548ab91535806707d71a36aab39f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119362491"
---
# <a name="jet_enumcolumnid-properties"></a>JET_ENUMCOLUMNID proprietà

Includere membri protetti  
Includere i membri ereditati  

Il [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) tipo espone i membri seguenti.

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
<td><a href="dn335141(v=exchg.10).md">columnid</a></td>
<td>Ottiene o imposta l'ID columnid da enumerare.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ctagSequence</a></td>
<td>Ottiene o imposta il numero di valori di colonna (in base all'indice in base uno) da enumerare per l'ID di colonna specificato. Se ctagSequence è 0 (zero), rgtagSequence viene ignorato e verranno enumerati tutti i valori di colonna per l'ID di colonna specificato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagSequence</a></td>
<td>Ottiene o imposta la matrice di indici in base uno nella matrice di valori di colonna per una determinata colonna. Un singolo elemento è un elemento itagSequence definito in JET_RETRIEVECOLUMN. Un valore itagSequence pari a 0 (zero) indica &quot; che ignora &quot; . Un valore itagSequence pari a 1 indica che restituisce il valore della prima colonna della colonna, 2 indica la seconda e così via.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_ENUMCOLUMNID classe](./jet-enumcolumnid-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
