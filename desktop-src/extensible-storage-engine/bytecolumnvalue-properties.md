---
description: Altre informazioni sulle proprietà ByteColumnValue
title: Proprietà ByteColumnValue
TOCTitle: ByteColumnValue properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.ByteColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytecolumnvalue_properties(v=EXCHG.10)
ms:contentKeyID: 55100961
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: d1c0a861cbc7adf7b1c0b9ea6f036b9ced6d14f7e8688e89d48c81c25b26554c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902117"
---
# <a name="bytecolumnvalue-properties"></a>Proprietà ByteColumnValue

Includere membri protetti  
Includere i membri ereditati  

Il [tipo ByteColumnValue](./bytecolumnvalue-class.md) espone i membri seguenti.

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
<td><a href="dn334166(v=exchg.10).md">Columnid</a></td>
<td>Ottiene o imposta l'elemento columnid da impostare o recuperare. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334212(v=exchg.10).md">Error (Errore) (Error (Errore)e)</a></td>
<td>Ottiene l'avviso generato dal recupero o dall'impostazione di questa colonna. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334165(v=exchg.10).md">ItagSequence</a></td>
<td>Ottiene o imposta la sequenza itag della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334225(v=exchg.10).md">Length</a></td>
<td>Ottiene la lunghezza in byte di un valore di colonna, ovvero zero se column è Null, in caso contrario corrisponde a Size per questa colonna di dimensioni fisse. Ereditato da <a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; </a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334169(v=exchg.10).md">RetrieveGrbit</a></td>
<td>Ottiene o imposta le opzioni di recupero della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334215(v=exchg.10).md">SetGrbit</a></td>
<td>Ottiene o imposta le opzioni di aggiornamento della colonna. Ereditato da <a href="dn334206(v=exchg.10).md">ColumnValue.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Proprietà protetta." alt="Protected property" /></td>
<td><a href="dn334116(v=exchg.10).md">Dimensioni</a></td>
<td>Ottiene le dimensioni del valore nella colonna. Viene restituito 0 per le colonne con dimensioni variabili, ad esempio binarie e stringa. Esegue l'override <a href="dn334172(v=exchg.10).md">di ColumnValue.Size.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334180(v=exchg.10).md">Valore</a></td>
<td>Ottiene o imposta il valore nello struct. Ereditato da <a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; </a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn334226(v=exchg.10).md">Oggetto ValueAsObject</a></td>
<td>Ottiene l'ultimo valore impostato o recuperato della colonna. Il valore viene restituito come oggetto generico. Ereditato da <a href="dn334171(v=exchg.10).md">ColumnValueOfStruct &lt; T &gt; </a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe ByteColumnValue](./bytecolumnvalue-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
