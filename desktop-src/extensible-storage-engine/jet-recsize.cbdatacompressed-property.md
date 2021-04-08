---
description: 'Altre informazioni su: Proprietà JET_RECSIZE. cbDataCompressed'
title: Proprietà JET_RECSIZE. cbDataCompressed (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'cbDataCompressed property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.cbdatacompressed(v=EXCHG.10)
ms:contentKeyID: 39515358
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.set_cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.cbDataCompressed
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.get_cbDataCompressed
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 747c2f00077f6a9d13de059f742bacc9a7936d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749823"
---
# <a name="jet_recsizecbdatacompressed-property"></a>Proprietà JET_RECSIZE. cbDataCompressed

Ottiene la dimensione compressa dei dati utente nel record. Si tratta dello stesso valore di [cbData](./jet-recsize.cbdata-property.md) se non vengono compressi valori Long intrinseci.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Property cbDataCompressed As Long
    Get
    Friend Set
'Usage
Dim instance As JET_RECSIZE
Dim value As Long

value = instance.cbDataCompressed
```

``` csharp
public long cbDataCompressed { get; internal set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System. Int64](/dotnet/api/system.int64)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_RECSIZE](./jet-recsize-structure2.md)

[Membri JET_RECSIZE](./jet-recsize-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)
