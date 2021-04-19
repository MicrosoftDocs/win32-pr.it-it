---
description: 'Altre informazioni su: Proprietà InstanceParameters. AlternateDatabaseRecoveryDirectory'
title: Proprietà InstanceParameters. AlternateDatabaseRecoveryDirectory
TOCTitle: 'AlternateDatabaseRecoveryDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.alternatedatabaserecoverydirectory(v=EXCHG.10)
ms:contentKeyID: 55107440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_AlternateDatabaseRecoveryDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70e08c65027806990ab511ef8561b41551f0ac2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308524"
---
# <a name="instanceparametersalternatedatabaserecoverydirectory-property"></a>Proprietà InstanceParameters. AlternateDatabaseRecoveryDirectory

Ottiene o imposta il percorso di file system relativo o assoluto di una cartella in cui il ripristino dell'arresto anomalo o un'operazione di ripristino è in grado di individuare i database a cui si fa riferimento nel log delle transazioni nella cartella specificata.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property AlternateDatabaseRecoveryDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.AlternateDatabaseRecoveryDirectory

instance.AlternateDatabaseRecoveryDirectory = value
```

``` csharp
public string AlternateDatabaseRecoveryDirectory { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. String](/dotnet/api/system.string)  

## <a name="remarks"></a>Commenti

Questo parametro viene ignorato in Windows XP.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
