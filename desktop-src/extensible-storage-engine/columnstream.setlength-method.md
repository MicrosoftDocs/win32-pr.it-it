---
description: Altre informazioni sul metodo ColumnStream.SetLength
title: Metodo ColumnStream.SetLength
TOCTitle: 'SetLength method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.SetLength(System.Int64)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.setlength(v=EXCHG.10)
ms:contentKeyID: 55100986
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.SetLength
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.SetLength
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5394341f097ad142398afa9ef40b848ee1ac5a33ecbe3d12bcf26b06e8022dfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670011"
---
# <a name="columnstreamsetlength-method"></a>Metodo ColumnStream.SetLength

Imposta la lunghezza del flusso.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Overrides Sub SetLength ( _
    value As Long _
)
'Usage
Dim instance As ColumnStream
Dim value As Long

instance.SetLength(value)
```

``` csharp
public override void SetLength(
    long value
)
```

#### <a name="parameters"></a>Parametri

  - Valore  
    Tipo: [System.Int64](/dotnet/api/system.int64)  
    
    Lunghezza desiderata, in byte.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe ColumnStream](./columnstream-class.md)

[Membri ColumnStream](./columnstream-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
