---
description: Altre informazioni sulla proprietà InstanceParameters.LogBuffers
title: InstanceParameters.LogBuffers - proprietà
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
ms.openlocfilehash: 60fbf06d13a8252051830c9a91dd348c2a7295a63212b587bfac9905b3b5903a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118255962"
---
# <a name="instanceparameterslogbuffers-property"></a>InstanceParameters.LogBuffers - proprietà

Ottiene o imposta la quantità di memoria utilizzata per memorizzare nella cache i record del log prima che siano scritti nel file di log delle transazioni. L'unità per questo parametro è la dimensione del settore del volume che contiene i file di log delle transazioni. Le dimensioni del settore sono quasi sempre di 512 byte, pertanto è sicuro presupporre che le dimensioni per l'unità. Questo parametro influisce sulle prestazioni. Quando il motore di database è in condizioni di carico di aggiornamento elevato, questo buffer può diventare pieno molto rapidamente. Una dimensione della cache maggiore per il file di log delle transazioni è fondamentale per prestazioni di aggiornamento ottimali in condizioni di carico così elevate. Il valore predefinito è noto come troppo piccolo per questo caso. Non impostare questo parametro su un numero di buffer maggiore (in byte) rispetto alla metà delle dimensioni di un file di log delle transazioni.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe InstanceParameters](./instanceparameters-class.md)

[Membri instanceParameters](./instanceparameters-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
