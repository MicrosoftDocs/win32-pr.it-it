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
ms.openlocfilehash: 1ff4588429d5b45690763c3f4eefd3553f88f480
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476657"
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
    
    SerializationInfo [che](/dotnet/api/system.runtime.serialization.serializationinfo) contiene i dati dell'oggetto serializzato relativi all'eccezione generata.

<!-- end list -->

  - contesto  
    Tipo: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)  
    
    StreamingContext [che](/dotnet/api/system.runtime.serialization.streamingcontext) contiene informazioni contestuali sull'origine o sulla destinazione.

#### <a name="implements"></a>Implementazioni

[ISerializable.GetObjectData(SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.serialization.iserializable.getobjectdata#System_Runtime_Serialization_ISerializable_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  
[_Exception.GetObjectData(SerializationInfo, StreamingContext)](/dotnet/api/system.runtime.interopservices._exception.getobjectdata#System_Runtime_InteropServices__Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  

## <a name="exceptions"></a>Eccezioni


| Eccezione | Condizione | 
|-----------|-----------|
| <a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a> | <p>Il parametro info è un riferimento null (Nothing in Visual Basic).</p> | 



## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe EsentErrorException](./esenterrorexception-class.md)

[Membri di EsentErrorException](./esenterrorexception-members.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
