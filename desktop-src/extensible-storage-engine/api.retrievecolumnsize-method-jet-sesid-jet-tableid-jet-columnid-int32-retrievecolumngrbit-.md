---
description: Altre informazioni sul metodo Api.RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
title: Metodo Api.RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100912
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53265560bab9d348d9631b8163aeb651b63026ed3797de7d32a91d7c462c4b8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117717990"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid-int32-retrievecolumngrbit"></a>Metodo Api.RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)

Recupera le dimensioni di un singolo valore di colonna dal record corrente. Il record è il record associato alla voce di indice nella posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati della colonna da una voce di indice che fa riferimento al record corrente.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    itagSequence As Integer, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim itagSequence As Integer
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid, itagSequence, _
    grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int itagSequence,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da usare.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore da cui recuperare la colonna.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Columnid da recuperare.

<!-- end list -->

  - itagSequence  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero di sequenza del valore in una colonna multivalore. La matrice di valori è in base uno. Il primo valore è la sequenza 1, non 0. Se la colonna del record ha un solo valore, è necessario passare 1 come itagSequence.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)  
    
    Recuperare le opzioni di colonna.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\>  
Dimensioni della colonna. 0 se la colonna è Null.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Overload di RetrieveColumnSize](./api.retrievecolumnsize-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
