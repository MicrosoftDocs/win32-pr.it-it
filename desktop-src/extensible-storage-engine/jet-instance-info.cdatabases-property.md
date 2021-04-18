---
description: 'Altre informazioni su: Proprietà JET_INSTANCE_INFO. cDatabases'
title: Proprietà JET_INSTANCE_INFO. cDatabases
TOCTitle: 'cDatabases property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.cDatabases
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.cdatabases(v=EXCHG.10)
ms:contentKeyID: 55103699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.cDatabases
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.set_cDatabases
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_cDatabases
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.cDatabases
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc6d81fc4389caf57ae5375a5548a1832b0cebfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319203"
---
# <a name="jet_instance_infocdatabases-property"></a>Proprietà JET_INSTANCE_INFO. cDatabases

Ottiene il numero di database collegati all'istanza del database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property cDatabases As Integer
    Get
    Private Set
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As Integer

value = instance.cDatabases
```

``` csharp
public int cDatabases { get; private set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_INSTANCE_INFO](./jet-instance-info-class.md)

[Membri JET_INSTANCE_INFO](./jet-instance-info-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
