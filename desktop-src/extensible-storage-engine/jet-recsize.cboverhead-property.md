---
description: 'Altre informazioni su: Proprietà JET_RECSIZE. cbOverhead'
title: Proprietà JET_RECSIZE. cbOverhead (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbOverhead property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cboverhead(v=EXCHG.10)
ms:contentKeyID: 39514763
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbOverhead
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbOverhead
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e7318428ef4b50a08a05f5021d293ad1d8d78cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305779"
---
# <a name="jet_recsizecboverhead-property"></a>Proprietà JET_RECSIZE. cbOverhead

Ottiene l'overhead della struttura di record ESENT per questo record. Sono incluse le dimensioni della chiave del record.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property cbOverhead As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbOverhead
```

``` csharp
public long cbOverhead { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_RECSIZE](./jet-recsize-structure2.md)

[Membri JET_RECSIZE](./jet-recsize-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
