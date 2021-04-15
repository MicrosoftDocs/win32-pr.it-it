---
description: 'Altre informazioni su: Metodo CimMofDeserializer. DeserializeClasses (byte [], UInt32, IEnumerable <CimClass> , String, String, OnClassNeeded, GetIncludedFileContent)'
title: Metodo CimMofDeserializer. DeserializeClasses (byte [], UInt32, IEnumerable (CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass), String, String, OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},System.String,System.String,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
ms.date: 11/14/2019
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
ms.openlocfilehash: 5772ca08a94c27e1ae0b110e05192004b9e4df2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524810"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-string-string-onclassneeded-getincludedfilecontent"></a>Metodo CimMofDeserializer. DeserializeClasses (byte \[ \] , UInt32, IEnumerable \<CimClass\> , String, String, OnClassNeeded, GetIncludedFileContent)

Deserializza le classi CIM in base ai dati serializzati, alla raccolta di classi CIM padre, ai nomi di computer e di spazi dei nomi e ai callback.

**Spazio dei nomi:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintassi

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes,
    string computerName,
    string namespaceName,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes,
    String^ computerName,
    String^ namespaceName,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> *
        computerName:string *
        namespaceName:string *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass),
    computerName As String,
    namespaceName As String,
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
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

<!-- end list -->

  - computerName  
    [System.String](/dotnet/api/system.string?view=netframework-4.8)
    
    Nome del computer.

<!-- end list -->

  - namespaceName  
    [System.String](/dotnet/api/system.string?view=netframework-4.8)
    
    Nome dello spazio dei nomi.

<!-- end list -->

  - onClassNeededCallback  
    Tipo: [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)
    
    Funzione di callback utilizzata per fornire un oggetto classe richiesto durante la deserializzazione.

<!-- end list -->

  - getIncludedFileCallback  
    Tipo: [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)
    
    Funzione di callback utilizzata per fornire il contenuto del buffer di file di un file specificato.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

Interfaccia [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) che può essere utilizzata per enumerare le classi CIM.

## <a name="see-also"></a>Vedi anche

[Classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[Spazio dei nomi Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
