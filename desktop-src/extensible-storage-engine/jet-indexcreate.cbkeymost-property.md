---
description: 'Altre informazioni su: JET_INDEXCREATE.cbKeyMost'
title: JET_INDEXCREATE.cbKeyMost
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
ms.openlocfilehash: 17908b19cba3ed047b98f4532982001019516d9b32e2799c29a6671cbd862fe7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119232681"
---
# <a name="jet_indexcreatecbkeymost-property"></a>JET_INDEXCREATE.cbKeyMost

Ottiene o imposta le dimensioni massime consentite, in byte, per le chiavi nell'indice. Le dimensioni massime minime supportate per la chiave JET_cbKeyMostMin (255), ovvero le dimensioni massime della chiave legacy. Le dimensioni massime della chiave dipendono dalle dimensioni della pagina del database [DatabasePageSize](./jet-param-enumeration.md). Le dimensioni massime della chiave possono essere recuperate con [KeyMost.](./systemparameters.keymost-property.md) Questo parametro viene ignorato in Windows XP e Windows Server 2003. A differenza dell'API non gestita, **IndexKeyMost()** (JET_bitIndexKeyMost) non è necessario, verrà aggiunto automaticamente.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

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

Tipo: [System.Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_INDEXCREATE classe](./jet-indexcreate-class.md)

[JET_INDEXCREATE membri](./jet-indexcreate-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
