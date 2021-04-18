---
description: 'Altre informazioni su: Proprietà InstanceParameters. LogBuffers'
title: Proprietà InstanceParameters. LogBuffers
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316500"
---
# <a name="instanceparameterslogbuffers-property"></a>Proprietà InstanceParameters. LogBuffers

Ottiene o imposta la quantità di memoria utilizzata per memorizzare nella cache i record del log prima che vengano scritti nel file di log delle transazioni. L'unità per questo parametro è la dimensione settoriale del volume che include i file di log delle transazioni. La dimensione del settore è quasi sempre di 512 byte, quindi è sicuro presupporre che le dimensioni dell'unità. Questo parametro ha un effetto sulle prestazioni. Quando il motore di database è sottoposto a un carico di aggiornamento intenso, questo buffer può essere pieno molto rapidamente. Una dimensione della cache maggiore per il file di log delle transazioni è essenziale per le prestazioni di aggiornamento ottimali in una condizione di carico elevato. Il valore predefinito è troppo piccolo per questo caso. Non impostare questo parametro su un numero di buffer maggiore (in byte) della metà delle dimensioni di un file di log delle transazioni.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri di InstanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
