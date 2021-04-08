---
description: 'Altre informazioni su: ColumnStream. Write (metodo)'
title: Metodo ColumnStream. Write
TOCTitle: 'Write method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.ColumnStream.Write(System.Byte[],System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnstream.write(v=EXCHG.10)
ms:contentKeyID: 55100987
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnStream.Write
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77b62e7dd028da3452082c973690ce0c0210b438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058172"
---
# <a name="columnstreamwrite-method"></a>Metodo ColumnStream. Write

Scrive una sequenza di byte nel flusso corrente e fa avanzare la posizione corrente nel flusso del numero di byte scritti.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Overrides Sub Write ( _
    buffer As Byte(), _
    offset As Integer, _
    count As Integer _
)
'Usage
Dim instance As ColumnStream
Dim buffer As Byte()
Dim offset As Integer
Dim count As Integer

instance.Write(buffer, offset, count)
```

``` csharp
public override void Write(
    byte[] buffer,
    int offset,
    int count
)
```

#### <a name="parameters"></a>Parametri

  - buffer  
    Tipo \[\]  
    
    Buffer da cui scrivere.

<!-- end list -->

  - offset  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Offset nel buffer da scrivere.

<!-- end list -->

  - count  
    Tipo: [System. Int32](/dotnet/api/system.int32)  
    
    Numero di byte da scrivere.

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe ColumnStream](./columnstream-class.md)

[Membri di ColumnStream](./columnstream-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
