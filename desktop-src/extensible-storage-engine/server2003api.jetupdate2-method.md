---
description: 'Altre informazioni su: Server2003Api. JetUpdate2, metodo'
title: Metodo Server2003Api. JetUpdate2 (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128155"
---
# <a name="server2003apijetupdate2-method"></a>Server2003Api. JetUpdate2, metodo

La funzione JetUpdate esegue un'operazione di aggiornamento, incluso l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente. L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
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

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. Server2003. UpdateGrbit](./updategrbit-enumeration.md)  
    
    Opzioni di aggiornamento.

## <a name="remarks"></a>Commenti

JetUpdate è il passaggio finale per eseguire un inserimento o un aggiornamento. L'aggiornamento viene avviato chiamando [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) e quindi chiamando [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o più volte per impostare lo stato del record. Infine, \[ \] per completare l'operazione di aggiornamento viene chiamato JetUpdate2 (JET_SESID, JET_TABLEID,, Int32, Int32, UpdateGrbit). Gli indici vengono aggiornati solo da JetUpdate o e non durante JetSetColumn.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Server2003Api](./server2003api-class.md)

[Membri di Server2003Api](./server2003api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
