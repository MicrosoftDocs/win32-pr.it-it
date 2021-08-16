---
description: Altre informazioni sul metodo Api.RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID)
title: Metodo Api.RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsFloat method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsFloat(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasfloat(v=EXCHG.10)
ms:contentKeyID: 55100846
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsFloat
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a388bd9d37d9502b512b59416ef9921f4eb5151369a181f3946e142b54285290
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118271732"
---
# <a name="apiretrievecolumnasfloat-method-jet_sesid-jet_tableid-jet_columnid"></a>Metodo Api.RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID)

Recupera un valore di colonna float dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function RetrieveColumnAsFloat ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Single)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Single)

returnValue = Api.RetrieveColumnAsFloat(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<float> RetrieveColumnAsFloat(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da usare.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore da cui recuperare la colonna.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid da recuperare.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Nullable](/dotnet/api/system.nullable-1)\<[Single](/dotnet/api/system.single)\>  
Dati recuperati dalla colonna come float. Null se la colonna è Null.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Overload di RetrieveColumnAsFloat](./api.retrievecolumnasfloat-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
