---
description: 'Altre informazioni su: Proprietà JET_DBINFOMISC. genCommitted'
title: Proprietà JET_DBINFOMISC. genCommitted
TOCTitle: 'genCommitted property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genCommitted
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.gencommitted(v=EXCHG.10)
ms:contentKeyID: 39513072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genCommitted
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genCommitted
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_genCommitted
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_genCommitted
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a40612c535bed3bbfe345add1fd922b65e450fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526095"
---
# <a name="jet_dbinfomiscgencommitted-property"></a>Proprietà JET_DBINFOMISC. genCommitted

Ottiene la generazione massima di log di cui è stato eseguito il commit nel database. In genere la generazione del log corrente.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property genCommitted As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.genCommitted
```

``` csharp
public int genCommitted { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_DBINFOMISC](./jet-dbinfomisc-class.md)

[Membri JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
