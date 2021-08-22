---
description: 'Altre informazioni su: Proprietà SystemParameters.StopFlushThreshold'
title: SystemParameters.StopFlushThreshold - proprietà
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
ms.openlocfilehash: e383123a5886b1cf2e978f8b2faac80feb8e9ceb7daaa051dd6b778a8c189ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118978461"
---
# <a name="systemparametersstopflushthreshold-property"></a>SystemParameters.StopFlushThreshold - proprietà

Ottiene o imposta la soglia in base alla quale la cache delle pagine del database termina la eliminazione delle pagine dalla cache per fare spazio alle pagine non memorizzate nella cache. Quando il numero di buffer di pagina nella cache supera questa soglia, il processo in background che è stato avviato per riempire il pool di buffer disponibili viene arrestato. Questa soglia è sempre relativa alla dimensione massima della cache impostata da JET_paramCacheSizeMax. Questa soglia deve anche essere sempre maggiore della soglia iniziale, come impostato da JET_paramStartFlushThreshold. La distanza tra la soglia di inizio e la soglia di arresto influisce sull'efficienza con cui le pagine del database vengono scaricate dal processo in background. Un gap maggiore rende più probabile che le scritture nelle pagine adiacenti possano essere combinate. Tuttavia, una soglia di arresto elevata ridurrà le dimensioni effettive della cache delle pagine del database.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[SystemParameters (classe)](./systemparameters-class.md)

[Membri di SystemParameters](./systemparameters-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
