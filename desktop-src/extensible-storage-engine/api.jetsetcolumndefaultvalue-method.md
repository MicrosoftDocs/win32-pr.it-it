---
description: 'Altre informazioni su: metodo API. JetSetColumnDefaultValue'
title: API. JetSetColumnDefaultValue, metodo
TOCTitle: 'JetSetColumnDefaultValue method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.SetColumnDefaultValueGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcolumndefaultvalue(v=EXCHG.10)
ms:contentKeyID: 55100802
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetColumnDefaultValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24fdb3a885e7aa558e1b3db3c4014fc65a28fcde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318828"
---
# <a name="apijetsetcolumndefaultvalue-method"></a>API. JetSetColumnDefaultValue, metodo

Modifica il valore predefinito di una colonna esistente.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetSetColumnDefaultValue ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    columnName As String, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As SetColumnDefaultValueGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim columnName As String
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As SetColumnDefaultValueGrbitApi.JetSetColumnDefaultValue(sesid, _
    dbid, tableName, columnName, data, _
    dataSize, grbit)
```

``` csharp
public static void JetSetColumnDefaultValue(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    string columnName,
    byte[] data,
    int dataSize,
    SetColumnDefaultValueGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Database contenente la colonna.

<!-- end list -->

  - tableName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nome della tabella contenente la colonna.

<!-- end list -->

  - columnName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nome della colonna.

<!-- end list -->

  - data  
    Tipo \[\]  
    
    Nuovo valore predefinito.

<!-- end list -->

  - dataSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Dimensioni del nuovo valore predefinito.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. SetColumnDefaultValueGrbit](./setcolumndefaultvaluegrbit-enumeration.md)  
    
    Opzioni del valore predefinito della colonna.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
