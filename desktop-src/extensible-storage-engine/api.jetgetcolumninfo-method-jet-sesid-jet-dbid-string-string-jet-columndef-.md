---
description: 'Altre informazioni su: Metodo Api.JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)'
title: Metodo Api.JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63eb642f035f9547d22946c1c800d0ad8b88d7aa6c363882a066dd230a2c7cf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042639"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columndef"></a>Metodo Api.JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)

Recupera informazioni su una colonna della tabella.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columndef As JET_COLUMNDEF _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columndef As JET_COLUMNDEFApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columndef)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNDEF columndef
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Database che contiene la tabella.

<!-- end list -->

  - tablename  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nome della tabella contenente la colonna.

<!-- end list -->

  - columnName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nome della colonna.

<!-- end list -->

  - columndef  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNDEF](./jet-columndef-class.md)  
    
    Compilato con informazioni sulla colonna.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Overload di JetGetColumnInfo](./api.jetgetcolumninfo-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
