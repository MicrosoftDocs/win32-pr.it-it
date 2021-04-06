---
description: 'Altre informazioni su: metodo API. JetIndexRecordCount'
title: API. JetIndexRecordCount, metodo
TOCTitle: 'JetIndexRecordCount method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetindexrecordcount(v=EXCHG.10)
ms:contentKeyID: 55100758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIndexRecordCount
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 429239ab7734a594fd2c5a3510650d8f410e94f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759428"
---
# <a name="apijetindexrecordcount-method"></a>API. JetIndexRecordCount, metodo

Conta il numero di voci nell'indice corrente dalla posizione corrente in poi. La posizione corrente è inclusa nel conteggio. Il conteggio può essere maggiore del numero totale di record nella tabella se l'indice corrente è su una colonna multivalore e le istanze della colonna hanno più valori. Se la tabella è vuota, verrà restituito 0 per il conteggio.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetIndexRecordCount ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef numRecords As Integer, _
    maxRecordsToCount As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numRecords As Integer
Dim maxRecordsToCount As IntegerApi.JetIndexRecordCount(sesid, _
    tableid, numRecords, maxRecordsToCount)
```

``` csharp
public static void JetIndexRecordCount(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out int numRecords,
    int maxRecordsToCount
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore in cui conteggiare i record.

<!-- end list -->

  - numRecords  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Restituisce il numero di record.

<!-- end list -->

  - maxRecordsToCount  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero massimo di record da contare. Il valore 0 indica che il conteggio è illimitato.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
