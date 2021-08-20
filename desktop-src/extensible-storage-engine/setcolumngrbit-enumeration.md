---
description: Altre informazioni sull'enumerazione SetColumnGrbit
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
ms.openlocfilehash: 8cfde1fe2bb0cefeb108cd957b043b14fc6b224375ae82b894eab0b9a0cb8865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071477"
---
# <a name="setcolumngrbit-enumeration"></a>Enumerazione SetColumnGrbit

Opzioni per JetSetColumn.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>Questa opzione viene usata per aggiungere dati a una colonna di tipo JET_coltypLongText o JET_coltypLongBinary. Lo stesso comportamento può essere ottenuto determinando le dimensioni del valore long esistente e specificando ibLongValue in psetinfo. Tuttavia, è più semplice usare questo grbit poiché non è necessario conoscere le dimensioni del valore di colonna esistente.</td>
</tr>
<tr class="odd">
<td></td>
<td>OverwriteLV</td>
<td>Questa opzione viene usata per sostituire il valore long esistente con i nuovi dati forniti. Quando si usa questa opzione, è come se il valore long esistente fosse stato impostato su una lunghezza pari a 0 (zero) prima di impostare i nuovi dati.</td>
</tr>
<tr class="even">
<td></td>
<td>RevertToDefaultValue</td>
<td>Questa opzione è applicabile solo alle colonne con tag, di tipo sparse o multivalore. Fa in modo che la colonna restituirà il valore predefinito della colonna nelle successive operazioni di recupero della colonna. Tutti i valori di colonna esistenti vengono rimossi.</td>
</tr>
<tr class="odd">
<td></td>
<td>SeparateLV</td>
<td>Questa opzione viene usata per forzare un valore long, colonne di tipo JET_coltyp. LongText o JET_coltyp. LongBinary, da archiviare separatamente dal resto dei dati del record. Ciò si verifica in genere quando le dimensioni del valore long ne impediscono l'archiviazione con i dati dei record rimanenti. Tuttavia, questa opzione può essere usata per forzare l'archiviazione separata del valore long. Si noti che non è possibile forzare la separazione di valori lunghi di quattro byte di dimensioni inferiori. In questi casi, l'opzione viene ignorata.</td>
</tr>
<tr class="even">
<td></td>
<td>SizeLV</td>
<td>Questa opzione viene usata per interpretare il buffer di input come numero intero di byte da impostare come lunghezza del valore long descritto da columnid specificato e, se specificato, il numero di sequenza in psetinfo- &gt; itagSequence. Se le dimensioni specificate sono maggiori del valore della colonna esistente, la colonna verrà estesa con 0. Se le dimensioni sono inferiori al valore della colonna esistente, il valore verrà troncato.</td>
</tr>
<tr class="odd">
<td></td>
<td>UniqueMultiValues</td>
<td>Questa opzione viene utilizzata per imporre che tutti i valori in una colonna multivalore siano distinti. Questa opzione confronta i dati della colonna di origine, senza alcuna trasformazione, con altri valori di colonna esistenti e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, non è possibile specificare anche AppendLV, OverwriteLV e SizeLV.</td>
</tr>
<tr class="even">
<td></td>
<td>UniqueNormalizedMultiValues</td>
<td>Questa opzione viene utilizzata per imporre che tutti i valori in una colonna multivalore siano distinti. Questa opzione confronta la trasformazione normalizzata della chiave dei dati della colonna con altri valori di colonna esistenti trasformati in modo analogo e viene restituito un errore se viene trovato un duplicato. Se viene specificata questa opzione, non è possibile specificare anche AppendLV, OverwriteLV e SizeLV.</td>
</tr>
<tr class="odd">
<td></td>
<td>ZeroLength</td>
<td>Questa opzione viene usata per impostare un valore di lunghezza zero. In genere, un valore di colonna viene impostato su NULL passando un valore cbMax pari a 0 (zero). Tuttavia, per alcuni tipi, ad esempio JET_coltyp. Testo, un valore di colonna può avere una lunghezza pari a 0 (zero) anziché NULL e questa opzione viene usata per distinguere tra NULL e lunghezza 0 (zero).</td>
</tr>
<tr class="even">
<td></td>
<td>IntrinsicLV</td>
<td>Provare a archiviare le colonne con valori lunghi nel record, anche se superano le dimensioni di separazione predefinite.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[Compressed](./windows7grbits.compressed-field.md)

[Non compresso](./windows7grbits.uncompressed-field.md)
