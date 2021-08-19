---
description: 'Altre informazioni su: Metodo ColumnStream.Seek'
title: Metodo ColumnStream.Seek
TOCTitle: 'Seek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Seek(System.Int64,System.IO.SeekOrigin)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.seek(v=EXCHG.10)
ms:contentKeyID: 55100949
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Seek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 883739bed33c17877dc86c33670233aab1afc67e9348009bb11c4e67ab27011c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119738191"
---
# <a name="columnstreamseek-method"></a>Metodo ColumnStream.Seek

Imposta la posizione all'interno del flusso corrente.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Overrides Function Seek ( _
    offset As Long, _
    origin As SeekOrigin _
) As Long
'Usage
Dim instance As ColumnStream
Dim offset As Long
Dim origin As SeekOrigin
Dim returnValue As Long

returnValue = instance.Seek(offset, origin)
```

``` csharp
public override long Seek(
    long offset,
    SeekOrigin origin
)
```

#### <a name="parameters"></a>Parametri

  - offset  
    Tipo: [System.Int64](/dotnet/api/system.int64)  
    
    Offset di byte relativo al parametro di origine.

<!-- end list -->

  - origin  
    Tipo: [System.IO.SeekOrigin](/dotnet/api/system.io.seekorigin)  
    
    SeekOrigin che indica il punto di riferimento per la nuova posizione.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Int64](/dotnet/api/system.int64)  
Nuova posizione nel flusso corrente.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe ColumnStream](./columnstream-class.md)

[Membri ColumnStream](./columnstream-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
