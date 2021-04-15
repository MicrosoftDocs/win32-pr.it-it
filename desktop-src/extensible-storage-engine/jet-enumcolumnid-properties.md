---
description: 'Altre informazioni su: Proprietà JET_ENUMCOLUMNID'
title: Proprietà JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525027"
---
# <a name="jet_enumcolumnid-properties"></a>Proprietà JET_ENUMCOLUMNID

Includi membri protetti  
Includi membri ereditati  

Il tipo di [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) espone i membri seguenti.

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
<td><a href="dn335141(v=exchg.10).md">ColumnID</a></td>
<td>Ottiene o imposta l'ID ColumnID da enumerare.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335092(v=exchg.10).md">ctagSequence</a></td>
<td>Ottiene o imposta il conteggio dei valori di colonna (in base a un indice in base 1) da enumerare per l'ID di colonna specificato. Se ctagSequence è 0 (zero), rgtagSequence viene ignorato e verranno enumerati tutti i valori di colonna per l'ID di colonna specificato.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335093(v=exchg.10).md">rgtagSequence</a></td>
<td>Ottiene o imposta la matrice di indici in base uno in una matrice di valori di colonna per una colonna specificata. Un singolo elemento è un itagSequence definito in JET_RETRIEVECOLUMN. Un itagSequence pari a 0 (zero) indica &quot; Skip &quot; . Un itagSequence di 1 indica che restituisce il primo valore della colonna, 2 indica il secondo e così via.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
