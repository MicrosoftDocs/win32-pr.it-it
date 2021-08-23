---
description: 'Altre informazioni su: JET_OSSNAPID. Metodo ToString (String, IFormatProvider)'
title: JET_OSSNAPID. Metodo ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512151
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 56e86765839434f2cd3a67c18f6395dd5443f21f8b905e6f86e6e85ad9915c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038869"
---
# <a name="jet_ossnapidtostring-method-string-iformatprovider"></a>JET_OSSNAPID. Metodo ToString (String, IFormatProvider)

Formatta il valore dell'istanza corrente usando il formato specificato.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_OSSNAPID
Dim format As String
Dim formatProvider As IFormatProvider
Dim returnValue As String

returnValue = instance.ToString(format, _
    formatProvider)
```

``` csharp
public string ToString(
    string format,
    IFormatProvider formatProvider
)
```

#### <a name="parameters"></a>Parametri

  - format  
    Tipo: [System.String](/dotnet/api/system.string)  
    
    Stringa [che](/dotnet/api/system.string) specifica il formato da usare. -oppure- Null per usare il formato predefinito definito per il tipo [dell'implementazione IFormattable.](/dotnet/api/system.iformattable)

<!-- end list -->

  - Formatprovider  
    Tipo: [System.IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    Oggetto [IFormatProvider](/dotnet/api/system.iformatprovider) da usare per formattare il valore. -oppure- Null per ottenere le informazioni sul formato numerico dalle impostazioni locali correnti del sistema operativo.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.String](/dotnet/api/system.string)  
Valore [String](/dotnet/api/system.string) contenente il valore dell'istanza corrente nel formato specificato.  

#### <a name="implements"></a>Implementazioni

[IFormattable.ToString(String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_OSSNAPID struttura](./jet-ossnapid-structure.md)

[JET_OSSNAPID membri](./jet-ossnapid-members.md)

[Overload di ToString](./jet-ossnapid.tostring-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
