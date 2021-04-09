---
description: 'Altre informazioni su: metodo API. GetTableIndexes (JET_SESID, JET_DBID, stringa)'
title: Metodo API. GetTableIndexes (JET_SESID, JET_DBID, String)
TOCTitle: GetTableIndexes method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55100648
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 90ac8dd014e0594fbffbb12b3ea4f3698f850de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878486"
---
# <a name="apigettableindexes-method-jet_sesid-jet_dbid-string"></a>Metodo API. GetTableIndexes (JET_SESID, JET_DBID, String)

Scorre tutti gli indici nella tabella, restituendo le informazioni su ognuna di esse.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Database contenente la tabella.

<!-- end list -->

  - tablename  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nome della tabella.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\>  
Iteratore su un IndexInfo per ogni indice nella tabella.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Overload GetTableIndexes](./api.gettableindexes-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
