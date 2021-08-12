---
description: 'Altre informazioni su: JET_SESID. Metodo ToString (String, IFormatProvider)'
title: JET_SESID. Metodo ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.tostring(v=EXCHG.10)
ms:contentKeyID: 39512468
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c8c750d2b05ecadc3cb900838b1b20b2c8f79e74ba61d50508dd7ae62dc66705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118253863"
---
# <a name="jet_sesidtostring-method-string-iformatprovider"></a>JET_SESID. Metodo ToString (String, IFormatProvider)

Formatta il valore dell'istanza corrente usando il formato specificato.

**Spazio dei**  [nomi: Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Function ToString ( _
    format As String, _
    formatProvider As IFormatProvider _
) As String
'Usage
Dim instance As JET_SESID
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
    
    Stringa [che](/dotnet/api/system.string) specifica il formato da usare. oppure null per usare il formato predefinito definito per il tipo [dell'implementazione di IFormattable.](/dotnet/api/system.iformattable)

<!-- end list -->

  - Formatprovider  
    Tipo: [System.IFormatProvider](/dotnet/api/system.iformatprovider)  
    
    Oggetto [IFormatProvider](/dotnet/api/system.iformatprovider) da usare per formattare il valore. oppure null per ottenere le informazioni sul formato numerico dalle impostazioni locali correnti del sistema operativo.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.String](/dotnet/api/system.string)  
Valore [String](/dotnet/api/system.string) contenente il valore dell'istanza corrente nel formato specificato.  

#### <a name="implements"></a>Implementazioni

[IFormattable.ToString(String, IFormatProvider)](/dotnet/api/system.iformattable.tostring#System_IFormattable_ToString_System_String_System_IFormatProvider_)  

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_SESID struttura](./jet-sesid-structure.md)

[JET_SESID membri](./jet-sesid-members.md)

[Overload di ToString](./jet-sesid.tostring-method2.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
