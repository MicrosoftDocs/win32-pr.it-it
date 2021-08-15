---
description: Altre informazioni sul metodo Api.JetGetSecondaryIndexBookmark
title: Metodo Api.JetGetSecondaryIndexBookmark
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a1ca2430ae188b256fb1c6d026db7b6d78e45fdbfeaec158242019b7795d910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042529"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a>Metodo Api.JetGetSecondaryIndexBookmark

Recupera un segnalibro speciale per la voce di indice secondaria nella posizione corrente di un cursore. Questo segnalibro può quindi essere usato per riposizionare in modo efficiente il cursore sulla stessa voce di indice usando JetGotoSecondaryIndexBookmark. Ciò è particolarmente utile quando si riposiziona in un indice secondario che contiene chiavi duplicate o che contiene più voci di indice per lo stesso record.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore da cui recuperare il segnalibro.

<!-- end list -->

  - secondaryKey  
    digitare: \[\]  
    
    Buffer di output per la chiave secondaria.

<!-- end list -->

  - secondaryKeySize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Dimensioni del buffer della chiave secondaria.

<!-- end list -->

  - actualSecondaryKeySize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Restituisce le dimensioni della chiave secondaria.

<!-- end list -->

  - primaryKey  
    digitare: \[\]  
    
    Buffer di output per la chiave primaria.

<!-- end list -->

  - primaryKeySize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Dimensioni del buffer della chiave primaria.

<!-- end list -->

  - actualPrimaryKeySize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Restituisce le dimensioni della chiave primaria.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)  
    
    Opzioni per la chiamata.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
