---
description: 'Altre informazioni su: Metodo Api.JetGetBookmark'
title: Metodo Api.JetGetBookmark
TOCTitle: 'JetGetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetbookmark(v=EXCHG.10)
ms:contentKeyID: 55100702
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d63bf41af250fcef6328433132fe64dcbdc862dcf8e35990c1ef1cbd02185e42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085480"
---
# <a name="apijetgetbookmark-method"></a>Metodo Api.JetGetBookmark

Recupera il segnalibro per il record associato alla voce di indice nella posizione corrente di un cursore. Questo segnalibro può quindi essere usato per riposizionare il cursore sullo stesso record usando [JetGotoBookmark(JET_SESID, JET_TABLEID, \[ \] , Int32).](./api.jetgotobookmark-method.md) Il segnalibro non sarà più lungo di [BookmarkMost](./systemparameters.bookmarkmost-property.md) bytes. Vedere anche [GetBookmark(JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetGetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetGetBookmark(sesid, tableid, _
    bookmark, bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetGetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
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

  - segnalibro  
    digitare: \[\]  
    
    Buffer in cui contenere il segnalibro.

<!-- end list -->

  - bookmarkSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Dimensioni del buffer del segnalibro.

<!-- end list -->

  - actualBookmarkSize  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Restituisce le dimensioni effettive del segnalibro.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
