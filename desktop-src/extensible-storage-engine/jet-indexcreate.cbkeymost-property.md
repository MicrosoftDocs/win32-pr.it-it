---
description: 'Altre informazioni su: Proprietà JET_INDEXCREATE. cbKeyMost'
title: Proprietà JET_INDEXCREATE. cbKeyMost
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55103646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.get_cbKeyMost
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.set_cbKeyMost
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 321704f88da59af33f4dab99d7d681fbcbd96e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883490"
---
# <a name="jet_indexcreatecbkeymost-property"></a>Proprietà JET_INDEXCREATE. cbKeyMost

Ottiene o imposta la dimensione massima consentita, in byte, per le chiavi nell'indice. Le dimensioni minime massime supportate per la chiave sono JET_cbKeyMostMin (255), ovvero le dimensioni massime della chiave legacy. Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database [DatabasePageSize](./jet-param-enumeration.md). È possibile recuperare le dimensioni massime della [chiave con la](./systemparameters.keymost-property.md)chiave. Questo parametro viene ignorato in Windows XP e Windows Server 2003. A differenza dell'API non gestita, **IndexKeyMost ()** (JET_bitIndexKeyMost) non è necessario, verrà aggiunto automaticamente.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_INDEXCREATE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_INDEXCREATE](./jet-indexcreate-class.md)

[Membri JET_INDEXCREATE](./jet-indexcreate-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
