---
description: 'Altre informazioni su: campo Server2003Grbits. EnumerateIgnoreUserDefinedDefault'
title: Campo Server2003Grbits. EnumerateIgnoreUserDefinedDefault (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: EnumerateIgnoreUserDefinedDefault field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits.enumerateignoreuserdefineddefault(v=EXCHG.10)
ms:contentKeyID: 55104099
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits.EnumerateIgnoreUserDefinedDefault
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 508565c518b67d31b0299014817b669f9484f743
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313070"
---
# <a name="server2003grbitsenumerateignoreuserdefineddefault-field"></a>Campo Server2003Grbits. EnumerateIgnoreUserDefinedDefault

Se una colonna specificata non è presente nel record e presenta un valore predefinito definito dall'utente, non verrà restituito alcun valore di colonna. Questa opzione impedisce al callback che calcola il valore predefinito definito dall'utente per la colonna di essere chiamato durante l'enumerazione dei valori per la colonna.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Const EnumerateIgnoreUserDefinedDefault As EnumerateColumnsGrbit
'Usage
Dim value As EnumerateColumnsGrbit

value = Server2003Grbits.EnumerateIgnoreUserDefinedDefault
```

``` csharp
public const EnumerateColumnsGrbit EnumerateIgnoreUserDefinedDefault
```

## <a name="remarks"></a>Osservazioni

Questa opzione è disponibile solo per i sistemi operativi Windows Server 2003 SP1 e versioni successive.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Server2003Grbits](./server2003grbits-class.md)

[Membri di Server2003Grbits](./server2003grbits-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
