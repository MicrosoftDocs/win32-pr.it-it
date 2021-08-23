---
description: Altre informazioni sul metodo Server2003Api.JetOSSnapshotAbort
title: Metodo Server2003Api.JetOSSnapshotAbort (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: 'JetOSSnapshotAbort method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetossnapshotabort(v=EXCHG.10)
ms:contentKeyID: 55104209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ca7633ce07468c7c516988e7e048b6c9673bc3ed685bbee35a4f5f094a59db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780221"
---
# <a name="server2003apijetossnapshotabort-method"></a>Metodo Server2003Api.JetOSSnapshotAbort

Notifica al motore che può riprendere le normali operazioni di I/O dopo un periodo di blocco terminato con uno snapshot non riuscito.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetOSSnapshotAbort ( _
    snapid As JET_OSSNAPID, _
    grbit As SnapshotAbortGrbit _
)
'Usage
Dim snapid As JET_OSSNAPID
Dim grbit As SnapshotAbortGrbitServer2003Api.JetOSSnapshotAbort(snapid, _
    grbit)
```

``` csharp
public static void JetOSSnapshotAbort(
    JET_OSSNAPID snapid,
    SnapshotAbortGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - snapid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificatore della sessione snapshot.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)  
    
    Opzioni per questa chiamata.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Server2003Api](./server2003api-class.md)

[Membri di Server2003Api](./server2003api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
