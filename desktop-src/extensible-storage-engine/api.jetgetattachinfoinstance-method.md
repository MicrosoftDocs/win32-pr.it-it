---
description: Altre informazioni sul metodo Api.JetGetAttachInfoInstance
title: Metodo Api.JetGetAttachInfoInstance
TOCTitle: 'JetGetAttachInfoInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String@,System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetattachinfoinstance(v=EXCHG.10)
ms:contentKeyID: 55100704
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetAttachInfoInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29796919302b19b708878feb31e1fd53151700694a67bd1f6943bfa9d82d419c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118272457"
---
# <a name="apijetgetattachinfoinstance-method"></a>Metodo Api.JetGetAttachInfoInstance

Utilizzato durante un backup avviato da [JetBeginExternalBackupInstance(JET_INSTANCE, BeginExternalBackupGrbit)](./api.jetbeginexternalbackupinstance-method.md) per eseguire una query su un'istanza per i nomi dei file di database che devono far parte del set di file di backup. Verranno considerati solo i database attualmente collegati all'istanza tramite [JetAttachDatabase(JET_SESID, String, AttachDatabaseGrbit).](./api.jetattachdatabase-method.md) Questi file possono essere successivamente aperti usando [JetOpenFileInstance(JET_INSTANCE, String, JET_HANDLE, Int64, Int64)](./api.jetopenfileinstance-method.md) e letti [usando JetReadFileInstance(JET_INSTANCE, JET_HANDLE, \[ \] , Int32, Int32).](./api.jetreadfileinstance-method.md)

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetGetAttachInfoInstance ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef files As String, _
    maxChars As Integer, _
    <OutAttribute> ByRef actualChars As Integer _
)
'Usage
Dim instance As JET_INSTANCE
Dim files As String
Dim maxChars As Integer
Dim actualChars As IntegerApi.JetGetAttachInfoInstance(instance, _
    files, maxChars, actualChars)
```

``` csharp
public static void JetGetAttachInfoInstance(
    JET_INSTANCE instance,
    out string files,
    int maxChars,
    out int actualChars
)
```

#### <a name="parameters"></a>Parametri

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Istanza di per cui ottenere le informazioni.

<!-- end list -->

  - files  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Restituisce un elenco di stringhe con terminazione Null che descrivono il set di file di database che devono far parte del set di file di backup. L'elenco di stringhe restituito in questo buffer è nello stesso formato di una stringa multipla usata dal Registro di sistema. Ogni stringa con terminazione Null viene restituita in sequenza seguita da un terminatore Null finale.

<!-- end list -->

  - maxChars  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Numero massimo di caratteri da recuperare.

<!-- end list -->

  - actualChars  
    Tipo: [System.Int32](/dotnet/api/system.int32)  
    
    Dimensioni effettive dell'elenco di file. Se è maggiore di maxChars, l'elenco è stato troncato.

## <a name="remarks"></a>Commenti

È importante notare che questa API non restituisce un errore o un avviso se il buffer di output è troppo piccolo per accettare l'elenco completo dei file che devono far parte del set di file di backup.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
