---
description: Altre informazioni sul metodo EsentErrorException.GetObjectData
title: Metodo EsentErrorException.GetObjectData
TOCTitle: 'GetObjectData method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.getobjectdata(v=EXCHG.10)
ms:contentKeyID: 55101432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7a4388d9af4f7cc6dbc284296b121fb3366e210c0d174a3db8e2b726f748f23a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784361"
---
# <a name="esenterrorexceptiongetobjectdata-method"></a>Metodo EsentErrorException.GetObjectData

Quando sottoposto a override in una classe derivata, imposta [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) con informazioni sull'eccezione.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
Public Overrides Sub GetObjectData ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim instance As EsentErrorException
Dim info As SerializationInfo
Dim context As StreamingContext

instance.GetObjectData(info, context)
```

``` csharp
public override void GetObjectData(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a>Parametri

  - info  
    Tipo: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)  
    
    SerializationInfo [che](/dotnet/api/system.runtime.serialization.serializationinfo) contiene i dati oggetto serializzati relativi all'eccezione generata.

<!-- end list -->

  - contesto  
    Tipo: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    StreamingContext [che](/dotnet/api/system.runtime.serialization.streamingcontext) contiene informazioni contestuali sull'origine o sulla destinazione.

#### <a name="implements"></a>Implementazioni

[ISerializable.GetObjectData(SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.serialization.iserializable.getobjectdata#System_Runtime_Serialization_ISerializable_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  
[_Exception.GetObjectData(SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.interopservices._exception.getobjectdata#System_Runtime_InteropServices__Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  

## <a name="exceptions"></a>Eccezioni

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Eccezione</th>
<th>Condizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a></td>
<td><p>Il parametro info è un riferimento null (Nothing in Visual Basic).</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe EsentErrorException](./esenterrorexception-class.md)

[Membri di EsentErrorException](./esenterrorexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
