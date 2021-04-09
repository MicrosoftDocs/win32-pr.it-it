---
description: 'Altre informazioni su: metodo API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Metodo API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: DeserializeObjectFromColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.deserializeobjectfromcolumn(v=EXCHG.10)
ms:contentKeyID: 55100688
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.DeserializeObjectFromColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9ec3ca1f505c9d768e54b284caf05b335934451
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878490"
---
# <a name="apideserializeobjectfromcolumn-method-jet_sesid-jet_tableid-jet_columnid"></a>Metodo API. DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)

Deserializzare un oggetto da una colonna.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function DeserializeObjectFromColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Object
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Object

returnValue = Api.DeserializeObjectFromColumn(sesid, _
    tableid, columnid)
```

``` csharp
public static Object DeserializeObjectFromColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabella da cui leggere.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Colonna da cui leggere.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Object](/dotnet/api/system.object)  
Oggetto deserializzato. Null se la colonna è null.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Overload DeserializeObjectFromColumn](./api.deserializeobjectfromcolumn-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
