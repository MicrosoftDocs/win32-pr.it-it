---
description: 'Altre informazioni su: JET_UNICODEINDEX. Metodo GetEffectiveLocaleName'
title: JET_UNICODEINDEX. Metodo GetEffectiveLocaleName
TOCTitle: 'GetEffectiveLocaleName method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.geteffectivelocalename(v=EXCHG.10)
ms:contentKeyID: 55103988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10932398e022701b76be19c3ea7949ce4cfd45b5a159ae5362e7f0e6a0e427bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118979081"
---
# <a name="jet_unicodeindexgeteffectivelocalename-method"></a>JET_UNICODEINDEX. Metodo GetEffectiveLocaleName

Come soluzione alternativa per i sistemi che non dispongono del supporto LCID, verrà convertito un numero molto limitato di LCID in nomi delle impostazioni locali.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function GetEffectiveLocaleName As String
'Usage
Dim instance As JET_UNICODEINDEX
Dim returnValue As String

returnValue = instance.GetEffectiveLocaleName()
```

``` csharp
public string GetEffectiveLocaleName()
```

#### <a name="return-value"></a>Valore restituito

Tipo: [System.String](/dotnet/api/system.string)  
Nome delle impostazioni locali in stile BCP-47.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_UNICODEINDEX classe](./jet-unicodeindex-class.md)

[JET_UNICODEINDEX membri](./jet-unicodeindex-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
