---
description: 'Altre informazioni su: metodo API. JetAttachDatabase2'
title: API. JetAttachDatabase2, metodo
TOCTitle: 'JetAttachDatabase2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.Int32,Microsoft.Isam.Esent.Interop.AttachDatabaseGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetattachdatabase2(v=EXCHG.10)
ms:contentKeyID: 55107224
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetAttachDatabase2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 33d91f0746b3ebf178bd61de58919ab99d85b1f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750770"
---
# <a name="apijetattachdatabase2-method"></a>API. JetAttachDatabase2, metodo

Associa un file di database per l'utilizzo con un'istanza di database. Per utilizzare il database, sarà necessario aprirlo successivamente con [JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)](./api.jetopendatabase-method.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function JetAttachDatabase2 ( _
    sesid As JET_SESID, _
    database As String, _
    maxPages As Integer, _
    grbit As AttachDatabaseGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim database As String
Dim maxPages As Integer
Dim grbit As AttachDatabaseGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetAttachDatabase2(sesid, _
    database, maxPages, grbit)
```

``` csharp
public static JET_wrn JetAttachDatabase2(
    JET_SESID sesid,
    string database,
    int maxPages,
    AttachDatabaseGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - database  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Database da aggiungere.

<!-- end list -->

  - maxPages  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Dimensione massima, in pagine del database, del database. Se il valore è 0, non viene applicato alcun valore massimo imposto.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. AttachDatabaseGrbit](./attachdatabasegrbit-enumeration.md)  
    
    Opzioni di connessione.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)  
Codice di avviso ESENT.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
