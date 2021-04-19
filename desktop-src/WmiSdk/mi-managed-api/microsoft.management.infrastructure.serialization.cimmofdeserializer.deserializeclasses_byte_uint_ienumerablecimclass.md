---
description: 'Altre informazioni su: Metodo CimMofDeserializer. DeserializeClasses (byte [], UInt32, IEnumerable <CimClass> )'
title: Metodo CimMofDeserializer. DeserializeClasses (byte [], UInt32, IEnumerable (CimClass)) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass)) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass})
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
ms.openlocfilehash: edcdb84e9c3a3fe7a070263385c9ee6551341152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317547"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass"></a>Metodo CimMofDeserializer. DeserializeClasses (byte \[ \] , UInt32, IEnumerable \<CimClass\> )

Deserializza le classi CIM basate sui dati serializzati e una raccolta di classi CIM padre.

**Spazio dei nomi:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintassi

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass)
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a>Parametri

  - serializedData  
    Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Buffer che contiene i dati serializzati.

<!-- end list -->

  - offset  
    Tipo: [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Offset dei byte nella posizione da cui iniziare la lettura dei dati. Quando il metodo restituisce un risultato, l'offset verrà puntato al byte successivo dopo le classi deserializzate.

<!-- end list -->

  - classi  
    Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>
    
    Cache facoltativa delle classi CIM padre.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

Interfaccia [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) che può essere utilizzata per enumerare le classi CIM.

## <a name="see-also"></a>Vedi anche

[Classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[Spazio dei nomi Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
