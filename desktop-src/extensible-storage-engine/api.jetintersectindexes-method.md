---
description: 'Altre informazioni su: metodo API. JetIntersectIndexes'
title: API. JetIntersectIndexes, metodo
TOCTitle: 'JetIntersectIndexes method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_INDEXRANGE[],System.Int32,Microsoft.Isam.Esent.Interop.JET_RECORDLIST@,Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetintersectindexes(v=EXCHG.10)
ms:contentKeyID: 55100761
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetIntersectIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3bae632f386ef944e79a17813d1cc86451441e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968644"
---
# <a name="apijetintersectindexes-method"></a>API. JetIntersectIndexes, metodo

Calcola l'intersezione tra più set di voci di indice da indici secondari diversi nella stessa tabella. Questa operazione è utile per trovare il set di record in una tabella che corrisponde a due o più criteri che possono essere espressi utilizzando intervalli di indice. Vedere anche [IntersectIndexes (JET_SESID, \[ \] )](./api.intersectindexes-method.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetIntersectIndexes ( _
    sesid As JET_SESID, _
    ranges As JET_INDEXRANGE(), _
    numRanges As Integer, _
    <OutAttribute> ByRef recordlist As JET_RECORDLIST, _
    grbit As IntersectIndexesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim ranges As JET_INDEXRANGE()
Dim numRanges As Integer
Dim recordlist As JET_RECORDLIST
Dim grbit As IntersectIndexesGrbitApi.JetIntersectIndexes(sesid, _
    ranges, numRanges, recordlist, grbit)
```

``` csharp
public static void JetIntersectIndexes(
    JET_SESID sesid,
    JET_INDEXRANGE[] ranges,
    int numRanges,
    out JET_RECORDLIST recordlist,
    IntersectIndexesGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - ranges  
    Tipo \[\]  
    
    Gli intervalli di indice da intersecare. Per TableIDs negli intervalli devono essere impostati intervalli di indice. Per creare un intervallo di indici, usare [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) .

<!-- end list -->

  - numRanges  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero di intervalli di indice.

<!-- end list -->

  - Recording  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)  
    
    Restituisce informazioni sulla tabella temporanea contenente i risultati dell'intersezione.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)  
    
    Opzioni di intersezione.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
