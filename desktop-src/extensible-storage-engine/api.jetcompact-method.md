---
description: 'Altre informazioni su: metodo API. JetCompact'
title: API. JetCompact, metodo
TOCTitle: 'JetCompact method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCompact(Microsoft.Isam.Esent.Interop.JET_SESID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS,Microsoft.Isam.Esent.Interop.JET_CONVERT,Microsoft.Isam.Esent.Interop.CompactGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcompact(v=EXCHG.10)
ms:contentKeyID: 55100666
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCompact
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74d714a1b0fa8d53743945afb3a35cc2015df293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966562"
---
# <a name="apijetcompact-method"></a>API. JetCompact, metodo

Crea una copia di un database esistente. La copia viene compattata in uno stato ottimale per l'utilizzo. I dati nei dati copiati verranno compressi in base alle misure scelte per gli indici in fase di creazione dell'indice. In questo modo, i dati compressi possono essere archiviati nel modo più denso possibile. In alternativa, i dati compressi possono riservare spazio per gli inserimenti di indici o di crescita successivi.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetCompact ( _
    sesid As JET_SESID, _
    sourceDatabase As String, _
    destinationDatabase As String, _
    statusCallback As JET_PFNSTATUS, _
    ignored As JET_CONVERT, _
    grbit As CompactGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim sourceDatabase As String
Dim destinationDatabase As String
Dim statusCallback As JET_PFNSTATUS
Dim ignored As JET_CONVERT
Dim grbit As CompactGrbitApi.JetCompact(sesid, sourceDatabase, _
    destinationDatabase, statusCallback, _
    ignored, grbit)
```

``` csharp
public static void JetCompact(
    JET_SESID sesid,
    string sourceDatabase,
    string destinationDatabase,
    JET_PFNSTATUS statusCallback,
    JET_CONVERT ignored,
    CompactGrbit grbit
)
```

#### <a name="parameters"></a>Parametri

  - sesid  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Sessione da utilizzare per la chiamata.

<!-- end list -->

  - sourceDatabase  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Database di origine che verrà compattato.

<!-- end list -->

  - destinationDatabase  
    Tipo: [System. String](/dotnet/api/system.string)  
    
    Nome da utilizzare per il database compresso.

<!-- end list -->

  - statusCallback  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Funzione di callback che può essere chiamata periodicamente tramite l'operazione di compattazione del database per segnalare lo stato di avanzamento.

<!-- end list -->

  - Ignorato  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_CONVERT](./jet-convert-class.md)  
    
    Questo parametro viene ignorato e deve essere null.

<!-- end list -->

  - grbit  
    Tipo: [Microsoft. ISAM. esent. Interop. CompactGrbit](./compactgrbit-enumeration.md)  
    
    Opzioni compatte.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
