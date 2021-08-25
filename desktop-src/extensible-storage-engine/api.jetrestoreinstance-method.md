---
description: Altre informazioni sul metodo Api.JetRestoreInstance
title: Metodo Api.JetRestoreInstance
TOCTitle: 'JetRestoreInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_PFNSTATUS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetrestoreinstance(v=EXCHG.10)
ms:contentKeyID: 55100787
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRestoreInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3fef9ca38f8e8efb86813666840f859ed10287197d5f3b6ed0bafdd434ea43dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947771"
---
# <a name="apijetrestoreinstance-method"></a>Metodo Api.JetRestoreInstance

Ripristina e ripristina un backup in streaming di un'istanza, inclusi tutti i database collegati. È progettato per funzionare con un backup creato con la funzione [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS).](./api.jetbackupinstance-method.md) Si tratta della funzione di ripristino più semplice e incapsulata.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Sub JetRestoreInstance ( _
    instance As JET_INSTANCE, _
    source As String, _
    destination As String, _
    statusCallback As JET_PFNSTATUS _
)
'Usage
Dim instance As JET_INSTANCE
Dim source As String
Dim destination As String
Dim statusCallback As JET_PFNSTATUSApi.JetRestoreInstance(instance, _
    source, destination, statusCallback)
```

``` csharp
public static void JetRestoreInstance(
    JET_INSTANCE instance,
    string source,
    string destination,
    JET_PFNSTATUS statusCallback
)
```

#### <a name="parameters"></a>Parametri

  - instance  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Istanza di da utilizzare. L'istanza di non deve essere inizializzata. Il ripristino dei file consente di inizializzare l'istanza di .

<!-- end list -->

  - source  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Percorso del backup. Il backup deve essere stato creato con [JetBackupInstance(JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)](./api.jetbackupinstance-method.md).

<!-- end list -->

  - destination  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Nome della cartella in cui verranno copiati e ripristinati i file di database del set di backup. Se questa proprietà è impostata su Null, i file di database verranno copiati e ripristinati nel percorso originale.

<!-- end list -->

  - statusCallback  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  
    
    Callback di notifica di stato facoltativo.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri api](./api-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
