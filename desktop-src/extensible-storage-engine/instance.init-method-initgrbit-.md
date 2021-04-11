---
description: 'Altre informazioni su: Metodo Instance.Init (InitGrbit)'
title: Metodo Instance.Init (InitGrbit)
TOCTitle: Init method (InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103295
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f87247a77cb89e6e5e9e20048b04f8d9fae36ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232604"
---
# <a name="instanceinit-method-initgrbit"></a>Metodo Instance.Init (InitGrbit)

Inizializzare il JET_INSTANCE.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim grbit As InitGrbit

instance.Init(grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    InitGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)  
    
    Opzioni di inizializzazione.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe dell'istanza](./instance-class.md)

[Membri di istanza](./instance-members.md)

[Overload init](./instance.init-method2.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
