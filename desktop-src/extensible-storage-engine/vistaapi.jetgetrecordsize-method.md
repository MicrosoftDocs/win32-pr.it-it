---
description: 'Altre informazioni su: VistaApi. JetGetRecordSize, metodo'
title: Metodo VistaApi. JetGetRecordSize (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetGetRecordSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE@,Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetrecordsize(v=EXCHG.10)
ms:contentKeyID: 55104285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37576e39d83270dcac3333e4d1f78fce32bb2669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307787"
---
# <a name="vistaapijetgetrecordsize-method"></a>VistaApi. JetGetRecordSize, metodo

Recupera le informazioni sulle dimensioni dei record dal percorso desiderato.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetGetRecordSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ByRef recsize As JET_RECSIZE, _
    grbit As GetRecordSizeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recsize As JET_RECSIZE
Dim grbit As GetRecordSizeGrbitVistaApi.JetGetRecordSize(sesid, tableid, _
    recsize, grbit)
```

``` csharp
public static void JetGetRecordSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ref JET_RECSIZE recsize,
    GetRecordSizeGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore che verrà usato per la chiamata API. Il cursore deve essere posizionato su un record o avere preparato un aggiornamento.

<!-- end list -->

  - recsize  
    Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Restituisce la dimensione del record.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)  
    
    Opzioni di chiamata.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe VistaApi](./vistaapi-class.md)

[Membri di VistaApi](./vistaapi-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
