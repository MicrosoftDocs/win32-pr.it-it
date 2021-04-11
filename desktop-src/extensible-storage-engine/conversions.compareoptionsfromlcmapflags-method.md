---
description: 'Altre informazioni su: Conversions. CompareOptionsFromLCMapFlags, metodo'
title: Conversions. CompareOptionsFromLCMapFlags, metodo
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
ms.openlocfilehash: 79e0d6a92aef75f3758adc16e9c82de81b8c6962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226414"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a>Conversions. CompareOptionsFromLCMapFlags, metodo

Flag specificati per LCMapFlags, trasformarli in opzioni di confronto. Le opzioni sconosciute vengono ignorate.

Questa API non è conforme a CLS. 

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
    Tipo: [System. UInt32](/dotnet/api/system.uint32)  
    
    Flag LCMapString.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
CompareOptions che descrive i flag (noti).  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Conversions](./conversions-class.md)

[Membri delle conversioni](./conversions-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
