---
description: Altre informazioni sul metodo Api.JetGetCurrentIndex
title: Metodo Api.JetGetCurrentIndex
TOCTitle: 'JetGetCurrentIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcurrentindex(v=EXCHG.10)
ms:contentKeyID: 55100699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCurrentIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 920c65f623d71656331a72ea0ab42d507c3498f585d93e903fa677866d92a1e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042609"
---
# <a name="apijetgetcurrentindex-method"></a>Metodo Api.JetGetCurrentIndex

Determina il nome dell'indice corrente di un determinato cursore. Questo nome viene usato anche per selezionare nuovamente l'indice come indice corrente usando [JetSetCurrentIndex(JET_SESID, JET_TABLEID, String).](./api.jetsetcurrentindex-method.md) Può anche essere usato per individuare le proprietà dell'indice usando JetGetTableIndexInfo.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetGetCurrentIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef indexName As String, _
    maxNameLength As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim maxNameLength As IntegerApi.JetGetCurrentIndex(sesid, tableid, _
    indexName, maxNameLength)
```

``` csharp
public static void JetGetCurrentIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string indexName,
    int maxNameLength
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Cursore per cui ottenere il nome dell'indice.

<!-- end list -->

  - indexName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Restituisce il nome dell'indice.

<!-- end list -->

  - maxNameLength  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Lunghezza massima del nome dell'indice. I nomi degli indici non sono più di [NameMost](./systemparameters.namemost-field.md) characters.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
