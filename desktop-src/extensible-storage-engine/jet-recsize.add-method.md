---
description: 'Altre informazioni su: JET_RECSIZE. Metodo Add'
title: JET_RECSIZE. Metodo Add (Microsoft.Isam.Esent.Interop.Vista)
TOCTitle: 'Add method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.add(v=EXCHG.10)
ms:contentKeyID: 39509872
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Add
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c14166f267a0a648c6ddf826f8c13277add9542a186010d015fc20e39ee4d5de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093471"
---
# <a name="jet_recsizeadd-method"></a>JET_RECSIZE. Metodo Add

Aggiungere le dimensioni in due JET_RECSIZE struttura .

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function Add ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Add(s1, s2)
```

``` csharp
public static JET_RECSIZE Add(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a>Parametri

  - s1  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Primo JET_RECSIZE.

<!-- end list -->

  - s2  
    Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
    
    Secondo oggetto JET_RECSIZE.

#### <a name="return-value"></a>Valore restituito

Tipo: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)  
Oggetto JET_RECSIZE contenente il risultato dell'aggiunta delle dimensioni in s1 e s2.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_RECSIZE struttura](./jet-recsize-structure2.md)

[JET_RECSIZE membri](./jet-recsize-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)
