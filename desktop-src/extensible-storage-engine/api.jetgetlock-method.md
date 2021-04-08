---
description: 'Altre informazioni su: metodo API. JetGetLock'
title: API. JetGetLock, metodo
TOCTitle: 'JetGetLock method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLock(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.GetLockGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetlock(v=EXCHG.10)
ms:contentKeyID: 55100732
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLock
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8480b6ac2eab84a0299e0bb3d480908e4f646fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878878"
---
# <a name="apijetgetlock-method"></a>API. JetGetLock, metodo

Riservare in modo esplicito la possibilità di aggiornare una riga, un blocco di scrittura o di impedire in modo esplicito l'aggiornamento di una riga da parte di qualsiasi altra sessione, blocco Read. In genere, i blocchi di scrittura di riga vengono acquisiti in modo implicito in seguito all'aggiornamento delle righe. I blocchi di lettura non sono in genere necessari a causa del controllo delle versioni dei record. Tuttavia, in alcuni casi è possibile che una transazione desideri bloccare in modo esplicito una riga per applicare la serializzazione o per assicurarsi che un'operazione successiva venga eseguita correttamente.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetGetLock ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As GetLockGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As GetLockGrbitApi.JetGetLock(sesid, tableid, grbit)
```

``` csharp
public static void JetGetLock(
    JET_SESID sesid,
    JET_TABLEID tableid,
    GetLockGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore da utilizzare. Verrà acquisito un blocco sul record corrente.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. GetLockGrbit](./getlockgrbit-enumeration.md)  
    
    Opzioni di blocco, utilizzare questa opzione per specificare il tipo di blocco da ottenere.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
