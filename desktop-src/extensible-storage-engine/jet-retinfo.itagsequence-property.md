---
description: 'Altre informazioni su: Proprietà JET_RETINFO. itagSequence'
title: Proprietà JET_RETINFO. itagSequence
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103876
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_itagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df42b6a52b34ec265aceb5b069b06f39c0663b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233640"
---
# <a name="jet_retinfoitagsequence-property"></a>Proprietà JET_RETINFO. itagSequence

Ottiene o imposta il numero di sequenza del valore in una colonna multivalore. La matrice di valori è in base uno. Il primo valore è Sequence 1, not 0. Se la colonna record ha un solo valore, è necessario passare 1 come itagSequence.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_RETINFO](./jet-retinfo-class.md)

[Membri JET_RETINFO](./jet-retinfo-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
