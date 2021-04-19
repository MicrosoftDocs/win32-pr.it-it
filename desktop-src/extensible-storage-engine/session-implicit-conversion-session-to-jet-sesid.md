---
description: 'Altre informazioni su: conversione implicita di sessione (sessione per JET_SESID)'
title: Conversione implicita di sessione (da sessione a JET_SESID)
TOCTitle: Implicit conversion (Session to JET_SESID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.op_Implicit(Microsoft.Isam.Esent.Interop.Session)~Microsoft.Isam.Esent.Interop.JET_SESID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.op_implicit(v=EXCHG.10)
ms:contentKeyID: 55104121
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Implicit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session.op_Implicit
- Microsoft.Isam.Esent.Interop.Session.Implicit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 512bc457a84ad1d1b170ac9d31cb04e36d8a05d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308487"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a>Conversione implicita di sessione (da sessione a JET_SESID)

Operatore di conversione implicito da una sessione a una JET_SESID. In questo modo è possibile usare una sessione con le API che prevedono un JET_SESID.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Widening Operator CType ( _
    session As Session _
) As JET_SESID
'Usage
Dim input As Session
Dim output As JET_SESID

output = CType(input, JET_SESID)
```

``` csharp
public static implicit operator JET_SESID (
    Session session
)
```

#### <a name="parameters"></a>Parametri

  - sessione  
    Tipo: [Microsoft. ISAM. esent. Interop. Session](./session-class.md)  
    
    Sessione da convertire.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
JET_SESID della sessione.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Session class](./session-class.md) (Classe di sessione)

[Membri della sessione](./session-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
