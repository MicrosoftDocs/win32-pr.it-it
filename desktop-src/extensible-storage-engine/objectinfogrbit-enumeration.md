---
description: Altre informazioni sull'enumerazione ObjectInfoGrbit
title: Enumerazione ObjectInfoGrbit
TOCTitle: ObjectInfoGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfogrbit(v=EXCHG.10)
ms:contentKeyID: 39516208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Bookmark
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Rollback
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit.Updatable
- Microsoft.Isam.Esent.Interop.ObjectInfoGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfd4bd427321137add1d0669fcaf798a353309a825d1ccf9544f45098d3454f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978641"
---
# <a name="objectinfogrbit-enumeration"></a>Enumerazione ObjectInfoGrbit

Opzioni di tabella, usate in [JET_OBJECTINFO](./jet-objectinfo-class.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoGrbit
'Usage
Dim instance As ObjectInfoGrbit
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoGrbit
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
<td>Segnalibro</td>
<td>La tabella può contenere segnalibri.</td>
</tr>
<tr class="even">
<td></td>
<td>Rollback</td>
<td>È possibile eseguire il rollback della tabella.</td>
</tr>
<tr class="odd">
<td></td>
<td>Aggiornabile</td>
<td>La tabella può essere aggiornata.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
