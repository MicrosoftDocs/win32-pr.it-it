---
description: 'Altre informazioni su: JET_ENUMCOLUMN proprietà'
title: JET_ENUMCOLUMN proprietà
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ee11c050d558fbefb15be4783a08b1808744718d043de038b297fdc5ebd9e3fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667921"
---
# <a name="jet_enumcolumn-properties"></a>JET_ENUMCOLUMN proprietà

Includere membri protetti  
Includere i membri ereditati  

Il [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) tipo espone i membri seguenti.

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
<td><a href="dn335137(v=exchg.10).md">cbData</a></td>
<td>Ottiene le dimensioni del valore enumerato per la colonna. Questo membro viene usato solo se <a href="dn335086(v=exchg.10).md">err</a> è uguale a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></td>
<td>Ottiene il numero di valori di colonna enumerati per la colonna. Questo membro viene usato solo se <a href="dn335086(v=exchg.10).md">err</a> non è <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">columnid</a></td>
<td>Ottiene l'ID columnid enumerato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">Err</a></td>
<td>Ottiene il codice di stato della colonna restituito dall'enumerazione .</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Ottiene il valore enumerato per la colonna. Questo membro viene usato solo se <a href="dn335086(v=exchg.10).md">err</a> è uguale a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>. Punta alla memoria allocata con il callback dell'allocatore <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> passato a <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>. Al termine, ricordarsi di rilasciare la memoria.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></td>
<td>Ottiene i valori di colonna enumerati per la colonna. Questo membro viene usato solo se <a href="dn335086(v=exchg.10).md">err</a> non è <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_ENUMCOLUMN classe](./jet-enumcolumn-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
