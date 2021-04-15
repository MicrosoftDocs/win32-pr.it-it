---
description: 'Altre informazioni su: metodo API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Metodo API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100792
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832e6d6cc123e4a85a2cacb2df688348732fcc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349601"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-int32-retrievecolumngrbit-jet_retinfo"></a>Metodo API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)

Recupera un valore di colonna singola dal record corrente. Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente. Oltre a recuperare il valore della colonna effettivo, è possibile utilizzare JetRetrieveColumn anche per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, actualDataSize, grbit, _
    retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - TableID  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore da cui recuperare la colonna.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    ColumnID da recuperare.

<!-- end list -->

  - data  
    Tipo \[\]  
    
    Buffer di dati in cui recuperare.

<!-- end list -->

  - dataSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Dimensioni del buffer di dati.

<!-- end list -->

  - dataOffset  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Offset nel buffer dei dati in cui leggere i dati.

<!-- end list -->

  - actualDataSize  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Restituisce le dimensioni effettive del buffer di dati.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Recupera le opzioni della colonna.

<!-- end list -->

  - retinfo  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)  
    
    Se pretinfo viene fornito come NULL, la funzione si comporta come se fosse stato specificato un itagSequence di 1 e un ibLongValue di 0 (zero). In questo modo il recupero della colonna Recupera il primo valore di una colonna multivalore e recupera i dati lunghi in corrispondenza dell'offset 0 (zero).

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Codice di avviso ESENT.  

## <a name="remarks"></a>Commenti

Si tratta di un metodo interno che accetta un offset del buffer e le dimensioni.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Overload JetRetrieveColumn](./api.jetretrievecolumn-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
