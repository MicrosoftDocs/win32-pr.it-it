---
description: 'Altre informazioni su: Conversions. ConvertDoubleToDateTime, metodo'
title: Conversions. ConvertDoubleToDateTime, metodo
TOCTitle: 'ConvertDoubleToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime(System.Double)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.convertdoubletodatetime(v=EXCHG.10)
ms:contentKeyID: 55101133
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.ConvertDoubleToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a1d066780ade3da95f4d4d5500143700f7a7d5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315707"
---
# <a name="conversionsconvertdoubletodatetime-method"></a>Conversions. ConvertDoubleToDateTime, metodo

Converte un valore Double (formato di data e ora di OA) in DateTime. Diversamente da DateTime. FromOADate, questa operazione non genera eccezioni.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Shared Function ConvertDoubleToDateTime ( _
    d As Double _
) As DateTime
'Usage
Dim d As Double
Dim returnValue As DateTime

returnValue = Conversions.ConvertDoubleToDateTime(d)
```

``` csharp
public static DateTime ConvertDoubleToDateTime(
    double d
)
```

#### <a name="parameters"></a>Parametri

  - d  
    Tipo: [System. Double](/dotnet/api/system.double)  
    
    Valore Double.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. DateTime](/dotnet/api/system.datetime)  
Valore DateTime.  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Conversions](./conversions-class.md)

[Membri delle conversioni](./conversions-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
