---
description: Altre informazioni sulla proprietà JET_DBINFOMISC.bkinfoIncPrev
title: JET_DBINFOMISC.bkinfoIncPrev
TOCTitle: 'bkinfoIncPrev property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.bkinfoincprev(v=EXCHG.10)
ms:contentKeyID: 39510848
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_bkinfoIncPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_bkinfoIncPrev
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.bkinfoIncPrev
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 454fabe8bd14dbab82b96b972838455e354f60d8cb07b4878c3733aac26f9dba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617581"
---
# <a name="jet_dbinfomiscbkinfoincprev-property"></a>JET_DBINFOMISC.bkinfoIncPrev

Ottiene informazioni sull'ultimo backup incrementale riuscito. Questo valore viene reimpostato quando è impostato [bkinfoFullPrev.](./jet-dbinfomisc.bkinfofullprev-property.md)

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property bkinfoIncPrev As JET_BKINFO
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_BKINFO

value = instance.bkinfoIncPrev
```

``` csharp
public JET_BKINFO bkinfoIncPrev { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_DBINFOMISC classe](./jet-dbinfomisc-class.md)

[JET_DBINFOMISC membri](./jet-dbinfomisc-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
