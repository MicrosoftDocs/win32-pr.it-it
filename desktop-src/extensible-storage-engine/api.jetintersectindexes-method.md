---
description: Altre informazioni sul metodo Api.JetIntersectIndexes
title: Metodo Api.JetIntersectIndexes
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
ms.openlocfilehash: 2b2e9e259d9c90a3067931fbba425ab1b21e5c2a36a73563f593d3b280a40496
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978031"
---
# <a name="apijetintersectindexes-method"></a>Metodo Api.JetIntersectIndexes

Calcola l'intersezione tra più set di voci di indice da indici secondari diversi sulla stessa tabella. Questa operazione è utile per trovare il set di record in una tabella che corrispondono a due o più criteri che possono essere espressi tramite intervalli di indici. Vedere anche [IntersectIndexes(JET_SESID, \[ \] )](./api.intersectindexes-method.md).

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - ranges  
    digitare: \[\]  
    
    Oggetto degli intervalli di indice da intersecare. Per gli id tabella negli intervalli devono essere impostati intervalli di indici. Usare [JetSetIndexRange(JET_SESID, JET_TABLEID SetIndexRangeGrbit)](./api.jetsetindexrange-method.md) per creare un intervallo di indici.

<!-- end list -->

  - NumRanges  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero di intervalli di indici.

<!-- end list -->

  - elenco record  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_RECORDLIST](./jet-recordlist-class.md)  
    
    Restituisce informazioni sulla tabella temporanea contenente i risultati dell'intersezione.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.IntersectIndexesGrbit](./intersectindexesgrbit-enumeration.md)  
    
    Opzioni di intersezione.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
