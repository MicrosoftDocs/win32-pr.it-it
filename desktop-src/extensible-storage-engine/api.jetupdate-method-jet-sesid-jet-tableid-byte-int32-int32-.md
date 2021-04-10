---
description: 'Altre informazioni su: metodo API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)'
title: Metodo API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879862"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a>Metodo API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)

La funzione JetUpdate esegue un'operazione di aggiornamento, incluso l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente. L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
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
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione che ha avviato l'aggiornamento.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore da aggiornare. È necessario preparare un aggiornamento.

<!-- end list -->

  - segnalibro  
    Tipo \[\]  
    
    Restituisce il segnalibro del record aggiornato. Può essere Null.

<!-- end list -->

  - bookmarkSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Dimensioni del buffer dei segnalibri.

<!-- end list -->

  - actualBookmarkSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Restituisce le dimensioni effettive del segnalibro.

## <a name="remarks"></a>Commenti

JetUpdate è il passaggio finale per eseguire un inserimento o un aggiornamento. L'aggiornamento viene avviato chiamando [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) e quindi chiamando [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o più volte per impostare lo stato del record. Infine, JetUpdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32) viene chiamato per completare l'operazione di aggiornamento. Gli indici vengono aggiornati solo da JetUpdate o e non durante JetSetColumn.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Overload JetUpdate](./api.jetupdate-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
