---
description: 'Altre informazioni su: Proprietà JET_THREADSTATS. cbLogRecord'
title: Proprietà JET_THREADSTATS. cbLogRecord (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbLogRecord property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cbLogRecord
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.cblogrecord(v=EXCHG.10)
ms:contentKeyID: 39511575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cbLogRecord
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.cbLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.get_cbLogRecord
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.set_cbLogRecord
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04325435f090d1549fe7e742e9d4554fb9c61720
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342676"
---
# <a name="jet_threadstatscblogrecord-property"></a>Proprietà JET_THREADSTATS. cbLogRecord

Ottiene le dimensioni totali, in byte, dei record del log delle transazioni generate dal motore di database sul thread corrente.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property cbLogRecord As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_THREADSTATS
Dim value As Integer

value = instance.cbLogRecord
```

``` csharp
public int cbLogRecord { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_THREADSTATS](./jet-threadstats-structure2.md)

[Membri JET_THREADSTATS](./jet-threadstats-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
