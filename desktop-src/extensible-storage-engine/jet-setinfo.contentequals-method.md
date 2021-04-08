---
description: 'Altre informazioni su: JET_SETINFO. Metodo ContentEquals'
title: JET_SETINFO. Metodo ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SETINFO.ContentEquals(Microsoft.Isam.Esent.Interop.JET_SETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103913
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETINFO.ContentEquals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e2e13ead56594c27eee6d269783c01f5b495ada
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049397"
---
# <a name="jet_setinfocontentequals-method"></a>JET_SETINFO. Metodo ContentEquals

Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_SETINFO _
) As Boolean
'Usage
Dim instance As JET_SETINFO
Dim other As JET_SETINFO
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_SETINFO other
)
```

#### <a name="parameters"></a>Parametri

  - altro  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_SETINFO](./jet-setinfo-class.md)  
    
    Istanza di da confrontare con questa istanza.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se le due istanze sono uguali.  

#### <a name="implements"></a>Implementazioni

[IContentEquatable \<T\> . ContentEquals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_SETINFO](./jet-setinfo-class.md)

[Membri JET_SETINFO](./jet-setinfo-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
