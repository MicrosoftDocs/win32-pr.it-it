---
description: Altre informazioni sulla proprietà SystemParameters.EnableAdvanced
title: Proprietà SystemParameters.EnableAdvanced
TOCTitle: 'EnableAdvanced property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.enableadvanced(v=EXCHG.10)
ms:contentKeyID: 55104116
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.set_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.get_EnableAdvanced
- Microsoft.Isam.Esent.Interop.SystemParameters.EnableAdvanced
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07fd683ad6f2f0d2a9afd88b46a7786131e15c370c9046945ad3e9594a533391
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107000"
---
# <a name="systemparametersenableadvanced-property"></a>Proprietà SystemParameters.EnableAdvanced

Ottiene o imposta un valore che indica se il motore di database accetta o rifiuta le modifiche apportate a un subset dei parametri di sistema. Questo parametro viene usato insieme a [Configuration](./systemparameters.configuration-property.md) per impedire l'impostazione di alcuni parametri di sistema rispetto alle impostazioni predefinite della configurazione selezionata. Supportato in Windows Vista e versioni seguenti. Ignorato Windows XP e Windows Server 2003.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Property EnableAdvanced As Boolean
    Get
    Set
'Usage
Dim value As Boolean

value = SystemParameters.EnableAdvanced

SystemParameters.EnableAdvanced = value
```

``` csharp
public static bool EnableAdvanced { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[SystemParameters (classe)](./systemparameters-class.md)

[Membri di SystemParameters](./systemparameters-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
