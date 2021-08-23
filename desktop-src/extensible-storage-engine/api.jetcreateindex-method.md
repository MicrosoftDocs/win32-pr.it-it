---
description: 'Altre informazioni su: Metodo Api.JetCreateIndex'
title: Metodo Api.JetCreateIndex
TOCTitle: 'JetCreateIndex method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateIndex(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.CreateIndexGrbit,System.String,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateindex(v=EXCHG.10)
ms:contentKeyID: 55100693
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateIndex
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df24e16252ec3aa837b9232859bf56726ee54b09448a57572281fab97a28c5c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670551"
---
# <a name="apijetcreateindex-method"></a>Metodo Api.JetCreateIndex

Crea un indice sui dati in un database ESE. Un indice può essere usato per individuare rapidamente dati specifici.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetCreateIndex ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexName As String, _
    grbit As CreateIndexGrbit, _
    keyDescription As String, _
    keyDescriptionLength As Integer, _
    density As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexName As String
Dim grbit As CreateIndexGrbit
Dim keyDescription As String
Dim keyDescriptionLength As Integer
Dim density As IntegerApi.JetCreateIndex(sesid, tableid, _
    indexName, grbit, keyDescription, _
    keyDescriptionLength, density)
```

``` csharp
public static void JetCreateIndex(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string indexName,
    CreateIndexGrbit grbit,
    string keyDescription,
    int keyDescriptionLength,
    int density
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare.

<!-- end list -->

  - tableid  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Tabella in cui creare l'indice.

<!-- end list -->

  - indexName  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Puntatore a una stringa con terminazione Null che specifica il nome dell'indice da creare.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft.Isam.Esent.Interop.CreateIndexGrbit](./createindexgrbit-enumeration.md)  
    
    Opzioni di creazione dell'indice.

<!-- end list -->

  - keyDescription  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Puntatore a una stringa con terminazione Null doppia di token delimitati da Null.

<!-- end list -->

  - keyDescriptionLength  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Lunghezza, in caratteri, di szKey, inclusi i due valori Null di terminazione.

<!-- end list -->

  - densità  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Densità iniziale dell'albero B+.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
