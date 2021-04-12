---
description: 'Altre informazioni su: metodo API. JetGetTruncateLogInfoInstance'
title: API. JetGetTruncateLogInfoInstance, metodo
TOCTitle: 'JetGetTruncateLogInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettruncateloginfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100743
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTruncateLogInfoInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc54d12796a724b382343c4a3514f03102df305f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233975"
---
# <a name="apijetgettruncateloginfoinstance-method"></a>API. JetGetTruncateLogInfoInstance, metodo

Utilizzato durante un backup avviato da [JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) per eseguire una query su un'istanza di per i nomi dei file di log delle transazioni che possono essere eliminati in modo sicuro dopo il completamento del backup.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetGetTruncateLogInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetTruncateLogInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetTruncateLogInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>Parametri

  - instance  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Istanza per cui ottenere le informazioni.

<!-- end list -->

  - files  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Restituisce un elenco di stringhe con terminazione null che descrivono il set di file di log del database che possono essere eliminati in modo sicuro al termine del backup. L'elenco di stringhe restituite in questo buffer è nello stesso formato di un multistringhe utilizzato dal registro di sistema. Ogni stringa con terminazione null viene restituita in sequenza seguita da un terminatore null finale.

<!-- end list -->

  - maxChars  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero massimo di caratteri da recuperare.

<!-- end list -->

  - actualChars  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Dimensioni effettive dell'elenco dei file. Se è maggiore di maxChars, l'elenco è stato troncato.

## <a name="remarks"></a>Commenti

È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
