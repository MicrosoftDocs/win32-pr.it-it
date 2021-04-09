---
description: 'Altre informazioni su: Proprietà InstanceParameters. CleanupMismatchedLogFiles'
title: Proprietà InstanceParameters. CleanupMismatchedLogFiles
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130558"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a>Proprietà InstanceParameters. CleanupMismatchedLogFiles

Ottiene o imposta un valore che indica se JetInit ha esito negativo quando il motore di database è configurato per iniziare a utilizzare i file di log delle transazioni su disco con dimensioni diverse da quelle configurate. In genere, [JetInit (JET_INSTANCE)](./api.jetinit-method.md) recupererà correttamente i database, ma avrà esito negativo con [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) per indicare che le dimensioni del file di log non sono configurate correttamente. Tuttavia, quando questo parametro è impostato su true, il motore di database eliminerà automaticamente tutti i vecchi file di log, avviando un nuovo set di file di log delle transazioni usando le dimensioni del file di log configurate. Questo parametro è utile quando l'applicazione desidera modificare in modo trasparente le dimensioni del file del log delle transazioni, ma continua a funzionare in modo trasparente negli scenari di aggiornamento e ripristino.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
