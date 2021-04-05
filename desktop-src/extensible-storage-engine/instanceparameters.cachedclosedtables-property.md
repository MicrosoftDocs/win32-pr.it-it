---
description: 'Altre informazioni su: Proprietà InstanceParameters. CachedClosedTables'
title: Proprietà InstanceParameters. CachedClosedTables
TOCTitle: 'CachedClosedTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55103293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CachedClosedTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f2465de2df3d25293f5298d40700512b6a086d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753975"
---
# <a name="instanceparameterscachedclosedtables-property"></a>Proprietà InstanceParameters. CachedClosedTables

Ottiene o imposta un valore che indica il numero di risorse dell'albero B + memorizzato nella cache dall'istanza dopo che le tabelle che rappresentano sono state chiuse dall'applicazione. I valori di grandi dimensioni per questo parametro comportano l'utilizzo di una maggiore quantità di memoria da parte del motore di database, ma aumentano la velocità con cui l'applicazione può aprire in modo casuale un numero elevato di tabelle. Questa operazione è utile per le applicazioni che dispongono di uno schema con un numero molto elevato di tabelle. Supportato in Windows Vista e in alto. Ignorato in Windows XP e Windows Server 2003.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property CachedClosedTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CachedClosedTables

instance.CachedClosedTables = value
```

``` csharp
public int CachedClosedTables { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
