---
description: 'Altre informazioni su: Metodo VistaApi.JetOSSnapshotTruncateLogInstance'
title: Metodo VistaApi.JetOSSnapshotTruncateLogInstance (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00a30d604aa57aeaff1d97ca8f92397d6919a769f9416eb504b2d22abe186f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471221"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a>Metodo VistaApi.JetOSSnapshotTruncateLogInstance

Tronca il log per un'istanza specificata durante una sessione snapshot.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - snapshot  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificatore dello snapshot.

<!-- end list -->

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Istanza di per cui troncare il log.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)  
    
    Opzioni per questa chiamata.

## <a name="remarks"></a>Commenti

Questa funzione deve essere chiamata solo se lo snapshot è stato creato con [l'opzione ContinueAfterThaw.](./vistagrbits.continueafterthaw-field.md) In caso contrario, la sessione snapshot termina dopo la chiamata a [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit).](./api.jetossnapshotthaw-method.md)

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe VistaApi](./vistaapi-class.md)

[Membri di VistaApi](./vistaapi-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
