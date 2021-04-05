---
description: 'Altre informazioni su: VistaApi. JetOSSnapshotEnd, metodo'
title: Metodo VistaApi. JetOSSnapshotEnd (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOSSnapshotEnd method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotend(v=EXCHG.10)
ms:contentKeyID: 55104196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 291d83929940a9f66f4e16c5088e6ec08187f908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752255"
---
# <a name="vistaapijetossnapshotend-method"></a>VistaApi. JetOSSnapshotEnd, metodo

Notifica al motore che la sessione snapshot è stata completata.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetOSSnapshotEnd ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotEndGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotEndGrbitVistaApi.JetOSSnapshotEnd(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotEnd(
    JET_OSSNAPID snapshot,
    SnapshotEndGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - snapshot  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificatore della sessione snapshot.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. vista. SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)  
    
    Opzioni di fine snapshot.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe VistaApi](./vistaapi-class.md)

[Membri di VistaApi](./vistaapi-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
