---
description: 'Altre informazioni su: Proprietà JET_ENUMCOLUMN'
title: Proprietà JET_ENUMCOLUMN
TOCTitle: JET_ENUMCOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103495
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 69d0822e12078a7990615ebd401fb63e474a389e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879177"
---
# <a name="jet_enumcolumn-properties"></a>Proprietà JET_ENUMCOLUMN

Includi membri protetti  
Includi membri ereditati  

Il tipo di [JET_ENUMCOLUMN](./jet-enumcolumn-class.md) espone i membri seguenti.

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
<td>Ottiene la dimensione del valore enumerato per la colonna. Questo membro viene utilizzato solo se <a href="dn335086(v=exchg.10).md">Err</a> è uguale a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335085(v=exchg.10).md">cEnumColumnValue</a></td>
<td>Ottiene il numero di valori di colonna enumerati per la colonna. Questo membro viene utilizzato solo se <a href="dn335086(v=exchg.10).md">Err</a> non è <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335135(v=exchg.10).md">ColumnID</a></td>
<td>Ottiene l'ID ColumnID enumerato.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335086(v=exchg.10).md">Err</a></td>
<td>Ottiene il codice di stato della colonna risultante dall'enumerazione.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335087(v=exchg.10).md">pvData</a></td>
<td>Ottiene il valore enumerato per la colonna. Questo membro viene utilizzato solo se <a href="dn335086(v=exchg.10).md">Err</a> è uguale a <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>. Questo fa riferimento alla memoria allocata con il callback dell'allocatore <a href="hh566077(v=exchg.10).md">JET_PFNREALLOC</a> passato a <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a>. Ricordarsi di rilasciare la memoria al termine dell'operazione.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn335089(v=exchg.10).md">rgEnumColumnValue</a></td>
<td>Ottiene i valori della colonna enumerata per la colonna. Questo membro viene utilizzato solo se <a href="dn335086(v=exchg.10).md">Err</a> non è <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_ENUMCOLUMN](./jet-enumcolumn-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
