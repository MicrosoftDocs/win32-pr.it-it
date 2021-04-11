---
description: 'Altre informazioni su: metodo API. JetDeleteTable'
title: API. JetDeleteTable, metodo
TOCTitle: 'JetDeleteTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDeleteTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdeletetable(v=EXCHG.10)
ms:contentKeyID: 55100683
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDeleteTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b4128ae81484343bec7fb4f52a736db149f0eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128715"
---
# <a name="apijetdeletetable-method"></a>API. JetDeleteTable, metodo

Elimina una tabella da un database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetDeleteTable ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    table As String _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim table As StringApi.JetDeleteTable(sesid, dbid, _
    table)
```

``` csharp
public static void JetDeleteTable(
    JET_SESID sesid,
    JET_DBID dbid,
    string table
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Database da cui eliminare la tabella.

<!-- end list -->

  - table  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nome della tabella da eliminare.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
