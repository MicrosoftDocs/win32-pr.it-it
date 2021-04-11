---
description: 'Altre informazioni su: Enumerazione MakeKeyGrbit'
title: Enumerazione MakeKeyGrbit
TOCTitle: MakeKeyGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.MakeKeyGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.makekeygrbit(v=EXCHG.10)
ms:contentKeyID: 39511453
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.None
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NormalizedKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.FullColumnStartLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.StrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.KeyDataZeroLength
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.NewKey
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnEndLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.SubStrLimit
- Microsoft.Isam.Esent.Interop.MakeKeyGrbit.PartialColumnStartLimit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c19a8c24b5adc4e8655c5372bd9c374e8674e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128626"
---
# <a name="makekeygrbit-enumeration"></a>Enumerazione MakeKeyGrbit

Opzioni per JetMakeKey.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration MakeKeyGrbit
'Usage
Dim instance As MakeKeyGrbit
```

``` csharp
[FlagsAttribute]
public enum MakeKeyGrbit
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
<td>NewKey</td>
<td>È necessario costruire una nuova chiave di ricerca. Qualsiasi chiave di ricerca precedentemente esistente viene eliminata.</td>
</tr>
<tr class="odd">
<td></td>
<td>NormalizedKey</td>
<td>Quando si specifica questa opzione, tutte le altre opzioni vengono ignorate, qualsiasi chiave di ricerca già esistente viene eliminata e il contenuto del buffer di input viene caricato come nuova chiave di ricerca.</td>
</tr>
<tr class="even">
<td></td>
<td>KeyDataZeroLength</td>
<td>Se la dimensione del buffer di input è zero e la colonna chiave corrente è una colonna a lunghezza variabile, questa opzione indica che il buffer di input contiene un valore di lunghezza zero. In caso contrario, una dimensione del buffer di input pari a zero indicherebbe un valore NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>StrLimit</td>
<td>Questa opzione indica che la chiave di ricerca deve essere costruita in modo tale che tutte le colonne chiave che vengono dopo la colonna chiave corrente devono essere considerate caratteri jolly.</td>
</tr>
<tr class="even">
<td></td>
<td>SubStrLimit</td>
<td>Questa opzione indica che la chiave di ricerca deve essere costruita in modo tale che la colonna chiave corrente venga considerata come un carattere jolly di prefisso e che tutte le colonne chiave che preentrano nella colonna chiave corrente siano considerate caratteri jolly.</td>
</tr>
<tr class="odd">
<td></td>
<td>FullColumnStartLimit</td>
<td>La chiave di ricerca deve essere costruita in modo tale che tutte le colonne chiave che vengono dopo la colonna chiave corrente devono essere considerate caratteri jolly.</td>
</tr>
<tr class="even">
<td></td>
<td>FullColumnEndLimit</td>
<td>La chiave di ricerca deve essere costruita in modo tale che tutte le colonne chiave che si trovano dopo la colonna chiave corrente siano considerate caratteri jolly.</td>
</tr>
<tr class="odd">
<td></td>
<td>PartialColumnStartLimit</td>
<td>La chiave di ricerca deve essere costruita in modo che la colonna chiave corrente sia considerata come un carattere jolly di prefisso e che tutte le colonne chiave successive alla colonna chiave corrente siano considerate caratteri jolly.</td>
</tr>
<tr class="even">
<td></td>
<td>PartialColumnEndLimit</td>
<td>La chiave di ricerca deve essere costruita in modo che la colonna chiave corrente sia considerata come un carattere jolly di prefisso e che tutte le colonne chiave successive alla colonna chiave corrente siano considerate caratteri jolly.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
