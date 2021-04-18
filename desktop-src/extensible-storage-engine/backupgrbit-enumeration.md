---
description: 'Altre informazioni su: Enumerazione BackupGrbit'
title: Enumerazione BackupGrbit
TOCTitle: BackupGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.BackupGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.backupgrbit(v=EXCHG.10)
ms:contentKeyID: 39512196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BackupGrbit.Incremental
- Microsoft.Isam.Esent.Interop.BackupGrbit
- Microsoft.Isam.Esent.Interop.BackupGrbit.Atomic
- Microsoft.Isam.Esent.Interop.BackupGrbit.None
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bda9754efcae8ebe353b8272ba57c5640ecdf946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318464"
---
# <a name="backupgrbit-enumeration"></a>Enumerazione BackupGrbit

Opzioni per [JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration BackupGrbit
'Usage
Dim instance As BackupGrbit
```

``` csharp
[FlagsAttribute]
public enum BackupGrbit
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
<td>Incremental</td>
<td>Crea un backup incrementale anziché un backup completo. Ciò significa che verrà eseguito il backup solo dei file di log creati dopo l'ultimo backup completo o incrementale.</td>
</tr>
<tr class="odd">
<td></td>
<td>Atomica</td>
<td>Crea un backup completo del database. In questo modo è possibile mantenere un backup esistente nella stessa directory se il nuovo backup non riesce.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
