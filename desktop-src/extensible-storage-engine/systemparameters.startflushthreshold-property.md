---
description: 'Altre informazioni su: Proprietà SystemParameters. StartFlushThreshold'
title: Proprietà SystemParameters. StartFlushThreshold
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
ms.openlocfilehash: 4a0e520682253d7a586c36366d229be59e014c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347971"
---
# <a name="systemparametersstartflushthreshold-property"></a>Proprietà SystemParameters. StartFlushThreshold

Ottiene o imposta la soglia in corrispondenza della quale la cache delle pagine del database inizia a rimuovere le pagine dalla cache per creare spazio per le pagine che non sono memorizzate nella cache. Quando il numero di buffer di pagina nella cache scende al di sotto di questa soglia, viene avviato un processo in background per ripristinare il pool di buffer disponibili. Questa soglia è sempre relativa alle dimensioni massime della cache impostate dal JET_paramCacheSizeMax. Anche questa soglia deve essere sempre inferiore alla soglia di arresto impostata dal JET_paramStopFlushThreshold. L'altezza della distanza della soglia iniziale determina il tempo di risposta che la cache delle pagine del database deve avere per produrre i buffer disponibili prima che siano necessari per l'applicazione. Una soglia di inizio elevata offrirà al processo in background più tempo per rispondere. Tuttavia, una soglia di avvio elevata implica una soglia di arresto superiore e che ridurrà le dimensioni effettive della cache delle pagine del database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[SystemParameters (classe)](./systemparameters-class.md)

[Membri SystemParameters](./systemparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
