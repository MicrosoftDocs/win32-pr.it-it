---
description: Altre informazioni sulla proprietà SystemParameters.StartFlushThreshold
title: SystemParameters.StartFlushThreshold - proprietà
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 49a868bf06f6994d61e3f901d5d9a447d2ef63c7909c33db3689fda343e16c27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484860"
---
# <a name="systemparametersstartflushthreshold-property"></a>SystemParameters.StartFlushThreshold - proprietà

Ottiene o imposta la soglia in base alla quale la cache delle pagine del database inizia a rimuovere le pagine dalla cache per fare spazio alle pagine non memorizzate nella cache. Quando il numero di buffer di pagina nella cache scende al di sotto di questa soglia, verrà avviato un processo in background per riempire il pool di buffer disponibili. Questa soglia è sempre relativa alla dimensione massima della cache impostata da JET_paramCacheSizeMax. Questa soglia deve essere sempre inferiore alla soglia di arresto impostata da JET_paramStopFlushThreshold. L'altezza della distanza della soglia di avvio determinerà il tempo di risposta che la cache della pagina del database deve avere per produrre buffer disponibili prima che l'applicazione ne abbia bisogno. Una soglia di avvio elevata offrirà al processo in background più tempo per reagire. Tuttavia, una soglia di avvio elevata implica una soglia di arresto più elevata che ridurrà le dimensioni effettive della cache delle pagine del database.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[SystemParameters (classe)](./systemparameters-class.md)

[Membri di SystemParameters](./systemparameters-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
