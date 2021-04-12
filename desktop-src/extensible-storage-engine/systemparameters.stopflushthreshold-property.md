---
description: 'Altre informazioni su: Proprietà SystemParameters. StopFlushThreshold'
title: Proprietà SystemParameters. StopFlushThreshold
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347966"
---
# <a name="systemparametersstopflushthreshold-property"></a>Proprietà SystemParameters. StopFlushThreshold

Ottiene o imposta la soglia in corrispondenza della quale la cache delle pagine del database smette di rimuovere le pagine dalla cache per creare spazio per le pagine non memorizzate nella cache. Quando il numero di buffer di pagina nella cache supera questa soglia, il processo in background che è stato avviato per ripristinare il pool di buffer disponibili viene arrestato. Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal JET_paramCacheSizeMax. Anche questa soglia deve essere sempre maggiore della soglia iniziale impostata da JET_paramStartFlushThreshold. La distanza tra la soglia iniziale e la soglia di arresto influiscono sull'efficienza con cui le pagine del database vengono scaricate dal processo in background. Un gap maggiore renderà più probabile che le Scritture nelle pagine adiacenti vengano combinate. Tuttavia, una soglia di arresto elevata ridurrà le dimensioni effettive della cache delle pagine del database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[SystemParameters (classe)](./systemparameters-class.md)

[Membri SystemParameters](./systemparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
