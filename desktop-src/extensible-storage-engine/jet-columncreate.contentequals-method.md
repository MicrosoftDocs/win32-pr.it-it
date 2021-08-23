---
description: 'Altre informazioni su: JET_COLUMNCREATE. Metodo ContentEquals'
title: JET_COLUMNCREATE. Metodo ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals(Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columncreate.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103471
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a61917bab1d39df3a3b448a51da8bd40bb055b726f444a9cdb23f30c986f248a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119668311"
---
# <a name="jet_columncreatecontentequals-method"></a>JET_COLUMNCREATE. Metodo ContentEquals

Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_COLUMNCREATE _
) As Boolean
'Usage
Dim instance As JET_COLUMNCREATE
Dim other As JET_COLUMNCREATE
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_COLUMNCREATE other
)
```

#### <a name="parameters"></a>Parametri

  - altro  
    Tipo: [Microsoft.Isam.Esent.Interop.JET_COLUMNCREATE](./jet-columncreate-class.md)  
    
    Istanza di da confrontare con questa istanza.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Boolean](/dotnet/api/system.boolean)  
True se le due istanze sono uguali.  

#### <a name="implements"></a>Implementazioni

[IContentEquatable \<T\> . ContentEquals(T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_COLUMNCREATE classe](./jet-columncreate-class.md)

[JET_COLUMNCREATE membri](./jet-columncreate-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
