---
description: 'Altre informazioni su: Proprietà JET_COLUMNDEF. CP'
title: Proprietà JET_COLUMNDEF. CP
TOCTitle: 'cp property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columndef.cp(v=EXCHG.10)
ms:contentKeyID: 55103411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.get_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.set_cp
- Microsoft.Isam.Esent.Interop.JET_COLUMNDEF.cp
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df383b212105a4b871f0c44d341d6113abf94d42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130550"
---
# <a name="jet_columndefcp-property"></a>Proprietà JET_COLUMNDEF. CP

Ottiene o imposta la tabella codici della colonna. Questa operazione è significativa solo per le colonne di tipo [Text](./jet-coltyp-enumeration.md) e [LONGTEXT](./jet-coltyp-enumeration.md).

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property cp As JET_CP
    Get
    Set
'Usage
Dim instance As JET_COLUMNDEF
Dim value As JET_CP

value = instance.cp

instance.cp = value
```

``` csharp
public JET_CP cp { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [Microsoft.ISAM.esent.Interop.JET_CP](./jet-cp-enumeration.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_COLUMNDEF](./jet-columndef-class.md)

[Membri JET_COLUMNDEF](./jet-columndef-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
