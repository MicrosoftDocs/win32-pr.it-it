---
description: 'Altre informazioni su: StringColumnValue Properties'
title: Proprietà di StringColumnValue
TOCTitle: StringColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.StringColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.stringcolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55104024
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 822e469fae8de69137cbbe7a8e085137c290850a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232139"
---
# <a name="stringcolumnvalue-properties"></a>Proprietà di StringColumnValue

Includi membri protetti  
Includi membri ereditati  

Il tipo [StringColumnValue](./stringcolumnvalue-class.md) espone i membri seguenti.

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
<td><a href="dn334166(v=exchg.10).md">ColumnID</a></td>
<td>Ottiene o imposta ColumnID da impostare o recuperare. Ereditato da <a href="dn334206(v=exchg.10).md">columnValue</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Error (Errore) (Error (Errore)e)</a></td>
<td>Ottiene l'avviso generato tramite il recupero o l'impostazione della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">columnValue</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Ottiene o imposta la sequenza ITag della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">columnValue</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351195(v=exchg.10).md">Length</a></td>
<td>Ottiene la lunghezza in byte di un valore di colonna, che è zero se la colonna è null; in caso contrario, corrisponde alla lunghezza in byte del valore stringa. La lunghezza in byte è determinata dal presupposto di due byte per carattere. Esegue l'override di <a href="dn334213(v=exchg.10).md">columnValue. length</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Ottiene o imposta le opzioni di recupero della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">columnValue</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Ottiene o imposta le opzioni di aggiornamento della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">columnValue</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Proprietà protetta." alt="Protected property" /></td>
<td><a href="dn351137(v=exchg.10).md">Dimensioni</a></td>
<td>Ottiene la dimensione del valore nella colonna. Viene restituito 0 per le colonne di dimensioni variabili, ad esempio binario e stringa. Esegue l'override di <a href="dn334172(v=exchg.10).md">columnValue. Size</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351204(v=exchg.10).md">Valore</a></td>
<td>Ottiene o imposta il valore della colonna. Utilizzare le <a href="dn334138(v=exchg.10).md">colonne (JET_SESID, JET_TABLEID, [])</a> per aggiornare un record con il valore della colonna.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351202(v=exchg.10).md">ValueAsObject</a></td>
<td>Ottiene l'ultimo valore impostato o recuperato della colonna. Il valore viene restituito come oggetto generico. Esegue l'override di <a href="dn334214(v=exchg.10).md">columnValue. ValueAsObject</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe StringColumnValue](./stringcolumnvalue-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
