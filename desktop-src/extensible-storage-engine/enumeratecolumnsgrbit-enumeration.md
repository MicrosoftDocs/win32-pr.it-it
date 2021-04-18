---
description: 'Altre informazioni su: Enumerazione EnumerateColumnsGrbit'
title: Enumerazione EnumerateColumnsGrbit
TOCTitle: EnumerateColumnsGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.enumeratecolumnsgrbit(v=EXCHG.10)
ms:contentKeyID: 39516754
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCompressOutput
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateIgnoreDefault
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.None
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateCopy
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumeratePresenceOnly
- Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit.EnumerateTaggedOnly
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e27e6810b37b513d550bbafce509b2815ccea2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318805"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>Enumerazione EnumerateColumnsGrbit

Opzioni per JetEnumerateColumns.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration EnumerateColumnsGrbit
'Usage
Dim instance As EnumerateColumnsGrbit
```

``` csharp
[FlagsAttribute]
public enum EnumerateColumnsGrbit
```

## <a name="members"></a>Members

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
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
<td>EnumerateCompressOutput</td>
<td>Quando si enumerano i valori di colonna, tutte le colonne per cui si recuperano tutti i valori e con un solo valore di colonna non NULL possono essere restituite in formato compresso. Lo stato di tali colonne verrà impostato su <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> e le dimensioni del valore della colonna e della memoria che contiene il valore della colonna verranno restituite direttamente nella struttura del <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> . Non è garantito che tutte le colonne idonee vengano compresse in questo modo. Per ulteriori informazioni, vedere <a href="dn335081(v=exchg.10).md">JET_ENUMCOLUMN</a> .</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumerateCopy</td>
<td>Questa opzione indica che è necessario enumerare i valori di colonna modificati del record anziché i valori di colonna originali. Se il valore di una colonna non è stato modificato, il valore della colonna originale viene enumerato. In questo modo, è possibile enumerare un valore di colonna che non è ancora stato inserito o aggiornato durante l'inserimento o l'aggiornamento di un record.
<p>Questa opzione è identica a <a href="hh578120(v=exchg.10).md">RetrieveCopy</a>.</p></td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateIgnoreDefault</td>
<td>Se una colonna specificata non è presente nel record, non verrà restituito alcun valore di colonna. In genere, il valore predefinito per la colonna, se presente, verrebbe restituito in questo caso. Si garantisce che se la colonna è impostata su un valore diverso da quello predefinito, verrà restituito un valore diverso, ovvero se una colonna con un valore predefinito viene impostata in modo esplicito su NULL, verrà restituito un valore NULL come valore per la colonna. Anche se questa opzione è richiesta, è comunque possibile visualizzare un valore di colonna che corrisponde al valore predefinito. Non viene effettuato alcun tentativo di rimuovere i valori di colonna che corrispondono ai valori predefiniti. È importante ricordare che questa opzione influisca sull'output di <a href="dn292148(v=exchg.10).md">JetEnumerateColumns (JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> se usato con EnumeratePresenceOnly o EnumerateTaggedOnly.</td>
</tr>
<tr class="odd">
<td></td>
<td>EnumeratePresenceOnly</td>
<td>Se è presente un valore non NULL per il valore della colonna o della colonna richiesta, i dati associati non vengono restituiti. Lo stato associato per quel valore di colonna o colonna verrà invece impostato su <a href="hh557250(v=exchg.10).md">ColumnPresent</a>. Se il valore della colonna o della colonna è NULL, <a href="hh557250(v=exchg.10).md">ColumnNull</a> verrà restituito come di consueto.</td>
</tr>
<tr class="even">
<td></td>
<td>EnumerateTaggedOnly</td>
<td>Quando si enumerano tutti i valori di colonna nel record, ad esempio quando numColumnids è zero, verranno restituiti solo i valori delle colonne con tag. Questa opzione non è consentita durante l'enumerazione di una matrice di ID di colonna specifica.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
