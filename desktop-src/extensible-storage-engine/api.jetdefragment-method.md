---
description: 'Altre informazioni su: metodo API. JetDefragment'
title: API. JetDefragment, metodo
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
ms.openlocfilehash: 69428d785bf9d607199cb62bfe02d2e373e7dbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306310"
---
# <a name="apijetdefragment-method"></a>API. JetDefragment, metodo

Avvia e arresta le attività di deframmentazione del database che migliorano l'organizzazione dei dati all'interno di un database.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare per la chiamata.

<!-- end list -->

  - dbid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Database da deframmentare.

<!-- end list -->

  - tableName  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Parametro non utilizzato. La deframmentazione viene eseguita per l'intero database descritto dall'ID del database specificato.

<!-- end list -->

  - passa  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Quando si avvia un'attività di deframmentazione in linea, questo parametro imposta il numero massimo di passaggi di deframmentazione. Quando si arresta un'attività di deframmentazione in linea, questo parametro viene impostato sul numero di passaggi eseguiti.

<!-- end list -->

  - secondi  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Quando si avvia un'attività di deframmentazione in linea, questo parametro imposta il tempo massimo per la deframmentazione. Quando si arresta un'attività di deframmentazione in linea, questo buffer di output viene impostato sul periodo di tempo utilizzato per la deframmentazione.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. DefragGrbit](./defraggrbit-enumeration.md)  
    
    Opzioni di deframmentazione.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Codice di avviso.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
