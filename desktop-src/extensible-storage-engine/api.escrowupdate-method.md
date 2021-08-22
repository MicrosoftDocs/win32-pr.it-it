---
description: Altre informazioni sul metodo Api.EscrowUpdate
title: Metodo Api.EscrowUpdate
TOCTitle: 'EscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.EscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.escrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100668
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e9bfaf180c67bea6da979877f9f768c850032adc2d085c4c65d47f3326442c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042729"
---
# <a name="apiescrowupdate-method"></a>Metodo Api.EscrowUpdate

Eseguire l'aggiunta atomica in una colonna. La colonna deve essere di tipo [Long.](./jet-coltyp-enumeration.md) Questa funzione consente a più sessioni di aggiornare lo stesso record contemporaneamente senza conflitti.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function EscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Integer _
) As Integer
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Integer
Dim returnValue As Integer

returnValue = Api.EscrowUpdate(sesid, _
    tableid, columnid, delta)
```

``` csharp
public static int EscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int delta
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da usare.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore da aggiornare.

<!-- end list -->

  - columnid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)  
    
    Colonna da aggiornare. Deve trattarsi di una colonna aggiornabile con deposito a garanzia.

<!-- end list -->

  - delta  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Delta da applicare alla colonna.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Int32](/dotnet/api/system.int32)  
Valore corrente della colonna archiviata nel database (il controllo delle versioni viene ignorato).  

## <a name="remarks"></a>Commenti

Questo metodo esegue il wrapping di [JetEscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, \[ \] , Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
