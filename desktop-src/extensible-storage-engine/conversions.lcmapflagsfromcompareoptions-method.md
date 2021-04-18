---
description: 'Altre informazioni su: Conversions. LCMapFlagsFromCompareOptions, metodo'
title: Conversions. LCMapFlagsFromCompareOptions, metodo
TOCTitle: 'LCMapFlagsFromCompareOptions method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions(System.Globalization.CompareOptions)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.lcmapflagsfromcompareoptions(v=EXCHG.10)
ms:contentKeyID: 55100974
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.LCMapFlagsFromCompareOptions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 55c034bb0e4e48217c5294d83f65b48245a5e455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308554"
---
# <a name="conversionslcmapflagsfromcompareoptions-method"></a>Conversions. LCMapFlagsFromCompareOptions, metodo

Assegnare a CompareOptions, trasformarli in flag da LCMapString. Le opzioni sconosciute vengono ignorate.

Questa API non è conforme a CLS. 

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function LCMapFlagsFromCompareOptions ( _
    compareOptions As CompareOptions _
) As UInteger
'Usage
Dim compareOptions As CompareOptions
Dim returnValue As UInteger

returnValue = Conversions.LCMapFlagsFromCompareOptions(compareOptions)
```

``` csharp
[CLSCompliantAttribute(false)]
public static uint LCMapFlagsFromCompareOptions(
    CompareOptions compareOptions
)
```

#### <a name="parameters"></a>Parametri

  - compareOptions  
    Tipo: [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
    
    Opzioni da convertire.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. UInt32](/dotnet/api/system.uint32)  
Flag LCMapString che corrispondono alle opzioni di confronto. Le opzioni non supportate vengono ignorate.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Conversions](./conversions-class.md)

[Membri delle conversioni](./conversions-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
