---
description: 'Altre informazioni su: JET_INDEXCREATE. Metodo ContentEquals'
title: JET_INDEXCREATE. Metodo ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_INDEXCREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103543
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXCREATE.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a607c191d53e14c8f5f8cdc88a8728467af18b2b1b502b37cdbdaf6ef9df991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117894938"
---
# <a name="jet_indexcreatecontentequals-method"></a>JET_INDEXCREATE. Metodo ContentEquals

Restituisce un valore che indica se questa istanza è uguale a un'altra istanza di .

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_INDEXCREATE _
) As Boolean
'Usage
Dim instance As JET_INDEXCREATE
Dim other As JET_INDEXCREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_INDEXCREATE other
)
```

#### <a name="parameters"></a>Parametri

  - altro  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_INDEXCREATE](./jet-indexcreate-class.md)  
    
    Istanza da confrontare con questa istanza.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se le due istanze sono uguali.  

#### <a name="implements"></a>Implementazioni

[Oggetto IContentEquatable. \<T\> ContentEquals(T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_INDEXCREATE classe](./jet-indexcreate-class.md)

[JET_INDEXCREATE membri](./jet-indexcreate-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
