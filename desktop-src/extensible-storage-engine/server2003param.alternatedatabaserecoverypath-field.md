---
description: 'Altre informazioni su: Campo Server2003Param.AlternateDatabaseRecoveryPath'
title: Campo Server2003Param.AlternateDatabaseRecoveryPath (Microsoft.Isam.Esent.Interop.Server2003)
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
ms.openlocfilehash: 4a85673979a3b65d8c78ca06fae4496c11f8d2b31c810d411142e6c40bfd62cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107244"
---
# <a name="server2003paramalternatedatabaserecoverypath-field"></a>Campo Server2003Param.AlternateDatabaseRecoveryPath

Il percorso completo di ogni database viene salvato in modo permanente nei log delle transazioni in fase di esecuzione. In genere, questi database devono rimanere nella posizione originale per il corretto funzionamento della riproduzione delle transazioni. Questo parametro può essere utilizzato per forzare il recupero con arresto anomalo del sistema o un'operazione di ripristino per cercare i database a cui si fa riferimento nel log delle transazioni nella cartella specificata.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
