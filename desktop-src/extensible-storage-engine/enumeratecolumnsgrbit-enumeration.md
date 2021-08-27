---
description: Altre informazioni sull'enumerazione EnumerateColumnsGrbit
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
ms.openlocfilehash: c1e6f768d2f8a837416540bcd3ca31f8984e55ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466808"
---
# <a name="enumeratecolumnsgrbit-enumeration"></a>Enumerazione EnumerateColumnsGrbit

Opzioni per JetEnumerateColumns.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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


|  | Nome del membro | Descrizione | 
|--|-------------|-------------|
|  | nessuno | Opzioni predefinite. | 
|  | EnumerateCompressOutput | Durante l'enumerazione dei valori di colonna, tutte le colonne per le quali vengono recuperati tutti i valori e che hanno un solo valore di colonna non NULL possono essere restituite in un formato compresso. Lo stato di tali colonne verrà impostato su <a href="hh557250(v=exchg.10).md">ColumnSingleValue</a> e le dimensioni del valore della colonna e la memoria contenente il valore della colonna verrà restituita direttamente nella <a href="dn335081(v=exchg.10).md">struttura JET_ENUMCOLUMN</a> colonna. Non è garantito che tutte le colonne idonee siano compresse in questo modo. Per <a href="dn335081(v=exchg.10).md">altre JET_ENUMCOLUMN,</a> vedere l'JET_ENUMCOLUMN. | 
|  | EnumerateCopy | Questa opzione indica che i valori di colonna modificati del record devono essere enumerati anziché i valori della colonna originale. Se un valore di colonna non è stato modificato, viene enumerato il valore originale della colonna. In questo modo, un valore di colonna che non è ancora stato inserito o aggiornato può essere enumerato durante l'inserimento o l'aggiornamento di un record.<p>Questa opzione è identica a <a href="hh578120(v=exchg.10).md">RetrieveCopy.</a></p> | 
|  | EnumerateIgnoreDefault | Se una determinata colonna non è presente nel record, non verrà restituito alcun valore di colonna. In genere, in questo caso viene restituito il valore predefinito per la colonna, se presente. È garantito che, se la colonna è impostata su un valore diverso da quello predefinito, verrà restituito un valore diverso, ovvero se una colonna con un valore predefinito è impostata in modo esplicito su NULL, come valore di tale colonna verrà restituito un valore NULL. Anche se questa opzione è richiesta, è comunque possibile visualizzare un valore di colonna che corrisponde al valore predefinito. Non è necessario rimuovere i valori di colonna che corrispondono ai valori predefiniti. È importante ricordare che questa opzione influisce sull'output di <a href="dn292148(v=exchg.10).md">JetEnumerateColumns(JET_SESID, JET_TABLEID, Int32, [], Int32, [], JET_PFNREALLOC, IntPtr, Int32, EnumerateColumnsGrbit)</a> se usata con EnumeratePresenceOnly o EnumerateTaggedOnly. | 
|  | EnumeratePresenceOnly | Se esiste un valore non NULL per la colonna o il valore di colonna richiesto, i dati associati non vengono restituiti. Al contrario, lo stato associato per tale colonna o valore di colonna verrà impostato su <a href="hh557250(v=exchg.10).md">ColumnPresent.</a> Se il valore della colonna o della colonna è NULL, <a href="hh557250(v=exchg.10).md">columnNull</a> verrà restituito come di consueto. | 
|  | EnumerateTaggedOnly | Quando si enumerano tutti i valori di colonna nel record, ad esempio quando numColumnids è zero, verranno restituiti solo i valori di colonna con tag. Questa opzione non è consentita durante l'enumerazione di una matrice specifica di ID di colonna. | 



## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[EnumerateIgnoreUserDefinedDefault](./server2003grbits.enumerateignoreuserdefineddefault-field.md)

[EnumerateInRecordOnly](./windows7grbits.enumerateinrecordonly-field.md)
