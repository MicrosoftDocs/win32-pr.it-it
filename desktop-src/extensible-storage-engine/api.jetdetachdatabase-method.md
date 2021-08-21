---
description: 'Altre informazioni su: Metodo Api.JetDetachDatabase'
title: Metodo Api.JetDetachDatabase
TOCTitle: 'JetDetachDatabase method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase(Microsoft.Isam.Esent.Interop.JET_SESID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdetachdatabase(v=EXCHG.10)
ms:contentKeyID: 55100687
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDetachDatabase
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 533c99c385f2e41825c312cf69e4205b7ab843c08b71b0618b21361b7b31ef50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085500"
---
# <a name="apijetdetachdatabase-method"></a>Metodo Api.JetDetachDatabase

Rilascia un file di database precedentemente collegato a una sessione di database.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetDetachDatabase ( _
    sesid As JET_SESID, _
    database As String _
)
'Usage
Dim sesid As JET_SESID
Dim database As StringApi.JetDetachDatabase(sesid, database)
```

``` csharp
public static void JetDetachDatabase(
    JET_SESID sesid,
    string database
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione di database da utilizzare.

<!-- end list -->

  - database  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Database da scollegare.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
