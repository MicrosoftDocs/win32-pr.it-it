---
description: 'Altre informazioni su: Enumerazione SetColumnGrbit'
title: Enumerazione SetColumnGrbit
TOCTitle: SetColumnGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.SetColumnGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.setcolumngrbit(v=EXCHG.10)
ms:contentKeyID: 39509934
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.RevertToDefaultValue
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.None
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.OverwriteLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SeparateLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueNormalizedMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.UniqueMultiValues
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.SizeLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.IntrinsicLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.AppendLV
- Microsoft.Isam.Esent.Interop.SetColumnGrbit.ZeroLength
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893f8e79b910a305bf6caccacd2d928e947be693
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485228"
---
# <a name="setcolumngrbit-enumeration"></a>Enumerazione SetColumnGrbit

Opzioni per JetSetColumn.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration SetColumnGrbit
'Usage
Dim instance As SetColumnGrbit
```

``` csharp
[FlagsAttribute]
public enum SetColumnGrbit
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome del membro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>nessuno</td>
<td>Opzioni predefinite.</td>
</tr>
<tr class="even">
<td></td>
<td>AppendLV</td>
<td>Questa opzione consente di accodare i dati a una colonna di tipo JET_coltypLongText o JET_coltypLongBinary. È possibile ottenere lo stesso comportamento determinando la dimensione del valore Long esistente e specificando ibLongValue in psetinfo. Tuttavia, è più semplice utilizzare questo grbit poiché la conoscenza della dimensione del valore della colonna esistente non è necessaria.</td>
</tr>
<tr class="odd">
<td></td>
<td>OverwriteLV</td>
<td>Questa opzione consente di sostituire il valore Long esistente con i dati appena forniti. Quando si utilizza questa opzione, è come se il valore Long esistente fosse stato impostato su 0 (zero) lunghezza prima dell'impostazione dei nuovi dati.</td>
</tr>
<tr class="even">
<td></td>
<td>RevertToDefaultValue</td>
<td>Questa opzione è applicabile solo per le colonne con tag, sparse o multivalore. Causa la restituzione del valore predefinito della colonna nelle successive operazioni di recupero della colonna. Tutti i valori di colonna esistenti vengono rimossi.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeparateLV</td>
<td>Questa opzione viene usata per forzare un valore Long, ovvero colonne di tipo JET_coltyp. LongText o JET_coltyp. LongBinary, da archiviare separatamente dal resto dei dati del record. Questa situazione si verifica in genere quando la dimensione del valore Long impedisce che venga archiviata con i dati dei record rimanenti. Tuttavia, questa opzione può essere usata per forzare l'archiviazione separata del valore Long. Si noti che non è possibile forzare la separazione dei valori long di quattro byte di dimensioni minori. In questi casi, l'opzione viene ignorata.</td>
</tr>
<tr class="even">
<td></td>
<td>SizeLV</td>
<td>Questa opzione viene usata per interpretare il buffer di input come numero intero di byte da impostare come lunghezza del valore Long descritto dal ColumnID specificato e, se specificato, il numero di sequenza in psetinfo- &gt; itagSequence. Se la dimensione specificata è maggiore del valore della colonna esistente, la colonna verrà estesa con 0. Se le dimensioni sono inferiori al valore della colonna esistente, il valore verrà troncato.</td>
</tr>
<tr class="odd">
<td></td>
<td>UniqueMultiValues</td>
<td>Questa opzione viene utilizzata per applicare che tutti i valori di una colonna multivalore sono distinti. Questa opzione consente di confrontare i dati della colonna di origine, senza alcuna trasformazione, con altri valori di colonna esistenti e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, non è possibile specificare anche AppendLV, OverwriteLV e SizeLV.</td>
</tr>
<tr class="even">
<td></td>
<td>UniqueNormalizedMultiValues</td>
<td>Questa opzione viene utilizzata per applicare che tutti i valori di una colonna multivalore sono distinti. Questa opzione Confronta la chiave di trasformazione normalizzata dei dati della colonna, ad altri valori di colonna esistenti trasformati in modo simile e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, non è possibile specificare anche AppendLV, OverwriteLV e SizeLV.</td>
</tr>
<tr class="odd">
<td></td>
<td>ZeroLength</td>
<td>Questa opzione viene utilizzata per impostare un valore su una lunghezza pari a zero. In genere, un valore di colonna è impostato su NULL passando un cbMax di 0 (zero). Tuttavia, per alcuni tipi, ad esempio JET_coltyp. Text, un valore di colonna può essere 0 (zero) Length anziché NULL e questa opzione viene usata per distinguere tra NULL e 0 (zero) Length.</td>
</tr>
<tr class="even">
<td></td>
<td>IntrinsicLV</td>
<td>Provare a archiviare le colonne con valore Long nel record, anche se superano le dimensioni di separazione predefinite.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[Compressed](./windows7grbits.compressed-field.md)

[Non compresso](./windows7grbits.uncompressed-field.md)
