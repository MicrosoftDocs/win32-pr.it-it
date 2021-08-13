---
description: 'Altre informazioni su: JET_THREADSTATS. Metodo Create'
title: JET_THREADSTATS. Metodo Create (Microsoft.Isam.Esent.Interop.Vista)
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
ms.openlocfilehash: 6a3450835a90c3e21902a6097d9cfb672c51769cc00810d86e338bef40ce2565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118251903"
---
# <a name="jet_threadstatscreate-method"></a>JET_THREADSTATS. Metodo Create

Creare un nuovo [JET_THREADSTATS](./jet-threadstats-structure2.md) struct con il valore specificato.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero di pagine visitate.

<!-- end list -->

  - cPageRead  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero di pagine lette.

<!-- end list -->

  - cPagePreread  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero di pagine già lette.

<!-- end list -->

  - cPageDirtied  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    TNumero di pagine non visualizzate.

<!-- end list -->

  - cPageRedirtied  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero di pagine non visualizzate.

<!-- end list -->

  - cLogRecord  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero di record di log generati.

<!-- end list -->

  - cbLogRecord  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Byte dei record di log scritti.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)  
Nuovo struct [JET_THREADSTATS](./jet-threadstats-structure2.md) con i valori specificati.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_THREADSTATS struttura](./jet-threadstats-structure2.md)

[JET_THREADSTATS membri](./jet-threadstats-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
