---
description: 'Altre informazioni su: costruttore di sessione'
title: Costruttore di sessione
TOCTitle: 'Session constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Session.#ctor(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session.session(v=EXCHG.10)
ms:contentKeyID: 55107728
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Session.Session
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Session..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 73d19d5ae1ba422969cd5b11f5b59ceb2811a89d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231789"
---
# <a name="session-constructor"></a>Costruttore di sessione

Inizializza una nuova istanza della classe Session. Una nuova JET_SESSION viene allocata dall'istanza di specificata.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Sub New ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCE

Dim instance As New Session(instance)
```

``` csharp
public Session(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a>Parametri

  - instance  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Istanza di in cui avviare la sessione.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Session class](./session-class.md) (Classe di sessione)

[Membri della sessione](./session-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
