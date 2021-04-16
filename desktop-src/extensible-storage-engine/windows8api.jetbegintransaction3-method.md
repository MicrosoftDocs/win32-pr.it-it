---
description: 'Altre informazioni su: Windows8Api. JetBeginTransaction3, metodo'
title: Metodo Windows8Api. JetBeginTransaction3 (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetBeginTransaction3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3(Microsoft.Isam.Esent.Interop.JET_SESID,System.Int64,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetbegintransaction3(v=EXCHG.10)
ms:contentKeyID: 55107825
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetBeginTransaction3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7605cdb44c66d929e6663caaad9e40d3c98737b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527720"
---
# <a name="windows8apijetbegintransaction3-method"></a>Windows8Api. JetBeginTransaction3, metodo

Consente a una sessione di immettere una transazione o di creare un nuovo punto di salvataggio in una transazione esistente.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetBeginTransaction3 ( _
    sesid As JET_SESID, _
    userTransactionId As Long, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim userTransactionId As Long
Dim grbit As BeginTransactionGrbitWindows8Api.JetBeginTransaction3(sesid, _
    userTransactionId, grbit)
```

``` csharp
public static void JetBeginTransaction3(
    JET_SESID sesid,
    long userTransactionId,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione per la quale iniziare la transazione.

<!-- end list -->

  - userTransactionId  
    Tipo: [System. Int64](/dotnet/api/system.int64)  
    
    Identificatore facoltativo fornito dall'utente per l'identificazione della transazione.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)  
    
    Opzioni di transazione.

## <a name="remarks"></a>Commenti

Introdotta in Windows 8.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Windows8Api](./windows8api-class.md)

[Membri di Windows8Api](./windows8api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
