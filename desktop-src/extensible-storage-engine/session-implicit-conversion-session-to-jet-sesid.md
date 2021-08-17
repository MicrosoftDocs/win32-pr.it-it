---
description: 'Altre informazioni su: Conversione implicita di sessione (da sessione a JET_SESID)'
title: Conversione implicita di sessione (da sessione JET_SESID)
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
ms.openlocfilehash: be293636044e744ec02e3bdcddbc96b61373a35c9bddc04a03d282fcebe268d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118485510"
---
# <a name="session-implicit-conversion-session-to-jet_sesid"></a>Conversione implicita di sessione (da sessione JET_SESID)

Operatore di conversione implicita da una sessione a una JET_SESID. In questo modo è possibile usare una sessione con le API che prevedono un JET_SESID.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.Isam.Esent.Interop.Session](./session-class.md)  
    
    Sessione da convertire.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
Oggetto JET_SESID della sessione.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Session class](./session-class.md) (Classe di sessione)

[Membri della sessione](./session-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
