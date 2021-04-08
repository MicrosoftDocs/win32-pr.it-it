---
description: 'Altre informazioni su: JET_RECPOS. Metodo ContentEquals'
title: JET_RECPOS. Metodo ContentEquals
TOCTitle: 'ContentEquals method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_RECPOS.ContentEquals(Microsoft.Isam.Esent.Interop.JET_RECPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_recpos.contentequals(v=EXCHG.10)
ms:contentKeyID: 55103845
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RECPOS.ContentEquals
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RECPOS.ContentEquals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cff822551bd2687308dde12df1f4e0e381f58046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883474"
---
# <a name="jet_recposcontentequals-method"></a>JET_RECPOS. Metodo ContentEquals

Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function ContentEquals ( _
    other As JET_RECPOS _
) As Boolean
'Usage
Dim instance As JET_RECPOS
Dim other As JET_RECPOS
Dim returnValue As Boolean

returnValue = instance.ContentEquals(other)
```

``` csharp
public bool ContentEquals(
    JET_RECPOS other
)
```

#### <a name="parameters"></a>Parametri

  - altro  
    Tipo: [Microsoft.ISAM.esent.Interop.JET_RECPOS](./jet-recpos-class.md)  
    
    Istanza di da confrontare con questa istanza.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Boolean](/dotnet/api/system.boolean)  
True se le due istanze sono uguali.  

#### <a name="implements"></a>Implementazioni

[IContentEquatable \<T\> . ContentEquals (T)](./icontentequatable-t-.contentequals-method.md)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_RECPOS](./jet-recpos-class.md)

[Membri JET_RECPOS](./jet-recpos-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
