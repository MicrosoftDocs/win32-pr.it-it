---
description: 'Altre informazioni su: JET_DBID. Metodo ToString (String, IFormatProvider)'
title: JET_DBID. Metodo ToString (String, IFormatProvider)
TOCTitle: ToString method (String, IFormatProvider)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.ToString(System.String,System.IFormatProvider)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.tostring(v=EXCHG.10)
ms:contentKeyID: 39513106
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.ToString
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b6fca1494a31bc342d4f8ad2933968c58efacc5f5e115ff10fe92a8afbabca8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017259"
---
# <a name="jet_dbidtostring-method-string-iformatprovider"></a>JET_DBID. Metodo ToString (String, IFormatProvider)

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
Dim instance As JET_DBID
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

[JET_DBID struttura](./jet-dbid-structure.md)

[JET_DBID membri](./jet-dbid-members.md)

[Overload di ToString](./jet-dbid.tostring-method.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
