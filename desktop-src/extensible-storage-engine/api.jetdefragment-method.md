---
description: Altre informazioni sul metodo Api.JetDefragment
title: Metodo Api.JetDefragment
TOCTitle: 'JetDefragment method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDefragment(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.Int32@,System.Int32@,Microsoft.Isam.Esent.Interop.DefragGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdefragment(v=EXCHG.10)
ms:contentKeyID: 55100679
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDefragment
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9761782e2c6522752d6a05f69005a4db6844542c700cbc5c942ea80d96bf4c2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272655"
---
# <a name="apijetdefragment-method"></a>Metodo Api.JetDefragment

Avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function JetDefragment ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tableName As String, _
    ByRef passes As Integer, _
    ByRef seconds As Integer, _
    grbit As DefragGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tableName As String
Dim passes As Integer
Dim seconds As Integer
Dim grbit As DefragGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetDefragment(sesid, _
    dbid, tableName, passes, seconds, _
    grbit)
```

``` csharp
public static JET_wrn JetDefragment(
    JET_SESID sesid,
    JET_DBID dbid,
    string tableName,
    ref int passes,
    ref int seconds,
    DefragGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare per la chiamata.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Database da deframmentare.

<!-- end list -->

  - tableName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Parametro non utilizzato. La deframmentazione viene eseguita per l'intero database descritto dall'ID database specificato.

<!-- end list -->

  - Passa  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Quando si avvia un'attività di deframmentazione online, questo parametro imposta il numero massimo di passaggi di deframmentazione. Quando si arresta un'attività di deframmentazione online, questo parametro viene impostato sul numero di passaggi eseguiti.

<!-- end list -->

  - secondi  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Quando si avvia un'attività di deframmentazione online, questo parametro imposta il tempo massimo per la deframmentazione. Quando si arresta un'attività di deframmentazione online, questo buffer di output viene impostato sul periodo di tempo usato per la deframmentazione.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.DefragGrbit](./defraggrbit-enumeration.md)  
    
    Opzioni di deframmentazione.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Codice di avviso.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
