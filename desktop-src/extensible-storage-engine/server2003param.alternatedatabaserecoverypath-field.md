---
description: 'Altre informazioni su: campo Server2003Param. AlternateDatabaseRecoveryPath'
title: Campo Server2003Param. AlternateDatabaseRecoveryPath (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: AlternateDatabaseRecoveryPath field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003param.alternatedatabaserecoverypath(v=EXCHG.10)
ms:contentKeyID: 55104217
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Param.AlternateDatabaseRecoveryPath
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 770ac27596b4385d0012cb65847754b4deb7e9fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308489"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a>Campo Server2003Param. AlternateDatabaseRecoveryPath

Il percorso completo di ogni database viene reso permanente nei log delle transazioni in fase di esecuzione. In genere, è necessario che questi database rimangano nel percorso originale affinché la riproduzione delle transazioni funzioni correttamente. Questo parametro può essere utilizzato per forzare il ripristino dell'arresto anomalo del sistema o un'operazione di ripristino per la ricerca dei database a cui si fa riferimento nel log delle transazioni nella cartella specificata.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Const AlternateDatabaseRecoveryPath As JET_param
'Usage
Dim value As JET_param

value = Server2003Param.AlternateDatabaseRecoveryPath
```

``` csharp
public const JET_param AlternateDatabaseRecoveryPath
```

## <a name="see-also"></a>Vedere anche

#### <a name="reference"></a>Riferimento

[Classe Server2003Param](./server2003param-class.md)

[Membri di Server2003Param](./server2003param-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
