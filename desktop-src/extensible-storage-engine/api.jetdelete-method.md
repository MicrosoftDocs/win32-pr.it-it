---
description: 'Altre informazioni su: metodo API. JetDelete'
title: API. JetDelete, metodo
TOCTitle: 'JetDelete method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDelete(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdelete(v=EXCHG.10)
ms:contentKeyID: 55100681
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbc3decf125b8d3f3f1df7228852901cca90aae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878886"
---
# <a name="apijetdelete-method"></a>API. JetDelete, metodo

Elimina il record corrente in una tabella di database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetDelete ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetDelete(sesid, tableid)
```

``` csharp
public static void JetDelete(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione che ha aperto il cursore.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore su una tabella di database. La riga corrente verrà eliminata.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
