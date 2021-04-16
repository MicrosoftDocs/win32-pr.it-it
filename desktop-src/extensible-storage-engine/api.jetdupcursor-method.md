---
description: 'Altre informazioni su: metodo API. JetDupCursor'
title: API. JetDupCursor, metodo
TOCTitle: 'JetDupCursor method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDupCursor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.DupCursorGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdupcursor(v=EXCHG.10)
ms:contentKeyID: 55100686
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDupCursor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fce19d23838f3dfeab5317bfa7ea1aaacfcb508
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525632"
---
# <a name="apijetdupcursor-method"></a>API. JetDupCursor, metodo

Duplica un cursore aperto e restituisce un handle per il cursore duplicato. Se il cursore duplicato era un cursore di sola lettura, il cursore duplicato è anche un cursore di sola lettura. Qualsiasi stato correlato alla costruzione di una chiave di ricerca o all'aggiornamento di un record non viene copiato nel cursore duplicato. Inoltre, la posizione del cursore originale non viene duplicata nel cursore duplicato. Il cursore duplicato viene sempre aperto nell'indice cluster e il relativo percorso è sempre nella prima riga della tabella.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetDupCursor ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef newTableid As JET_TABLEID, _
    grbit As DupCursorGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim newTableid As JET_TABLEID
Dim grbit As DupCursorGrbitApi.JetDupCursor(sesid, tableid, _
    newTableid, grbit)
```

``` csharp
public static void JetDupCursor(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_TABLEID newTableid,
    DupCursorGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore da duplicare.

<!-- end list -->

  - newTableid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore duplicato.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. DupCursorGrbit](./dupcursorgrbit-enumeration.md)  
    
    Riservato per utilizzi futuri.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
