---
description: 'Altre informazioni su: JET_TABLEID. Metodo ToString (String, IFormatProvider)'
title: JET_TABLEID. Metodo ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.tostring(v=EXCHG.10)
ms:contentKeyID: 39510805
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.ToString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e8d57d572a44f04c5b76ffb11f5243f7afb2b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315635"
---
# <a name="jet_tableidtostring-method-string-iformatprovider"></a>JET_TABLEID. Metodo ToString (String, IFormatProvider)

Formatta il valore dell'istanza corrente usando il formato specificato.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_TABLEID
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
    Tipo: [System. String](/dotnet/api/system.string)  
    
    [Stringa](/dotnet/api/system.string) che specifica il formato da utilizzare. oppure null per usare il formato predefinito definito per il tipo dell'implementazione di [IFormattable](/dotnet/api/system.iformattable) .

<!-- end list -->

  - formatProvider  
    Tipo: [System. IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    [IFormatProvider](/dotnet/api/system.iformatprovider) da utilizzare per formattare il valore. oppure, null per ottenere le informazioni sul formato numerico dalle impostazioni locali correnti del sistema operativo.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. String](/dotnet/api/system.string)  
[Stringa](/dotnet/api/system.string) contenente il valore dell'istanza corrente nel formato specificato.  

#### <a name="implements"></a>Implementazioni

[IFormattable. ToString (String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Struttura JET_TABLEID](./jet-tableid-structure.md)

[Membri JET_TABLEID](./jet-tableid-members.md)

[Overload ToString](./jet-tableid.tostring-method.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
