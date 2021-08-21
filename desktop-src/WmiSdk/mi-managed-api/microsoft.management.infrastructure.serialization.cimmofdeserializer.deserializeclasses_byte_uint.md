---
description: 'Altre informazioni su: Metodo CimMofDeserializer.DeserializeClasses (Byte[], UInt32)'
title: Metodo CimMofDeserializer.DeserializeClasses (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@)
ms.date: 11/13/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: b05a1eca97c650b130170af2c6c03a958b6022017902e39f15156b08038bad08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317412"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32"></a>Metodo CimMofDeserializer.DeserializeClasses (Byte \[ \] , UInt32)

Deserializza le classi CIM in base ai dati serializzati.

**Spazio dei nomi:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintassi

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a>Parametri

  - serializedData  
    Tipo: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Buffer contenente i dati serializzati.

<!-- end list -->

  - offset  
    Tipo: [System.UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Offset di byte nella posizione in cui iniziare a leggere i dati. Quando il metodo viene restituito, l'offset punta al byte successivo dopo le classi deserializzate.

#### <a name="return-value"></a>Valore restituito

Tipo: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

Interfaccia [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) che può essere usata per enumerare le classi CIM.

## <a name="see-also"></a>Vedi anche

[Classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[Spazio dei nomi Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
