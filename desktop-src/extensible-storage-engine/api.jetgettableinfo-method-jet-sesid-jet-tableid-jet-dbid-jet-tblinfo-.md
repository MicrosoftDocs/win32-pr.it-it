---
description: 'Altre informazioni su: metodo API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)'
title: Metodo API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_DBID@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100736
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e955a1b854162bd8eca4e19506329c2cf6016e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316967"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-jet_dbid-jet_tblinfo"></a>Metodo API. JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)

Recupera varie informazioni su una tabella in un database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As JET_DBID, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As JET_DBID
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_DBID result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabella per cui recuperare le informazioni.

<!-- end list -->

  - result  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Informazioni recuperate.

<!-- end list -->

  - infoLevel  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)  
    
    Tipo di informazioni da recuperare.

## <a name="remarks"></a>Commenti

Questo overload viene utilizzato con [dbid](./jet-tblinfo-enumeration.md).

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Overload JetGetTableInfo](./api.jetgettableinfo-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
