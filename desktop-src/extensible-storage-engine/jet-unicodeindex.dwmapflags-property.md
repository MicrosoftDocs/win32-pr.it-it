---
description: Altre informazioni sulla proprietà JET_UNICODEINDEX.dwMapFlags
title: JET_UNICODEINDEX.dwMapFlags
TOCTitle: 'dwMapFlags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.dwmapflags(v=EXCHG.10)
ms:contentKeyID: 55103990
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.set_dwMapFlags
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.get_dwMapFlags
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e7f7be15a52948a269544b606d90a290f129ff262240ddc92e33a67c9b24fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117892116"
---
# <a name="jet_unicodeindexdwmapflags-property"></a>JET_UNICODEINDEX.dwMapFlags

Ottiene o imposta i flag da utilizzare con LCMapString durante la normalizzazione dei dati Unicode.

Questa API non è conforme a CLS. 

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Property dwMapFlags As UInteger
    Get
    Set
'Usage
Dim instance As JET_UNICODEINDEX
Dim value As UInteger

value = instance.dwMapFlags

instance.dwMapFlags = value
```

``` csharp
[CLSCompliantAttribute(false)]
public uint dwMapFlags { get; set; }
```

#### <a name="property-value"></a>Valore proprietà

Tipo: [System.UInt32](/dotnet/api/system.uint32)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_UNICODEINDEX classe](./jet-unicodeindex-class.md)

[JET_UNICODEINDEX membri](./jet-unicodeindex-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
