---
description: 'Altre informazioni su: JET_THREADSTATS. Metodo Create'
title: JET_THREADSTATS. Metodo Create (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758492"
---
# <a name="jet_threadstatscreate-method"></a>JET_THREADSTATS. Metodo Create

Crea una nuova struttura di [JET_THREADSTATS](./jet-threadstats-structure2.md) con il valore specificato.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a>Parametri

  - cPageReferenced  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero di pagine visitate.

<!-- end list -->

  - cPageRead  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero di pagine lette.

<!-- end list -->

  - cPagePreread  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero di pagine prelette.

<!-- end list -->

  - cPageDirtied  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    TNumber delle pagine sporche.

<!-- end list -->

  - cPageRedirtied  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero di pagine risporche.

<!-- end list -->

  - cLogRecord  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero di record di log generati.

<!-- end list -->

  - cbLogRecord  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Byte dei record di log scritti.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Nuovo [JET_THREADSTATS](./jet-threadstats-structure2.md) struct con i valori specificati.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_THREADSTATS](./jet-threadstats-structure2.md)

[Membri JET_THREADSTATS](./jet-threadstats-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
