---
description: Altre informazioni sul metodo Conversions.CompareOptionsFromLCMapFlags
title: Metodo Conversions.CompareOptionsFromLCMapFlags
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfe3a65c52d23ee335a81560775f0063b8ca81a10cc43c1787e353a5b803eed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117901847"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a>Metodo Conversions.CompareOptionsFromLCMapFlags

Dati i flag per LCMapFlags, trasformarli in opzioni di confronto. Le opzioni sconosciute vengono ignorate.

Questa API non è conforme a CLS. 

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a>Parametri

  - lcmapFlags  
    Tipo: [System.UInt32](/dotnet/api/system.uint32)  
    
    Flag LCMapString.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Globalization.CompareOptions](/dotnet/api/system.globalization.compareoptions)  
CompareOptions che descrive i flag (noti).  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Conversions](./conversions-class.md)

[Membri delle conversioni](./conversions-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
