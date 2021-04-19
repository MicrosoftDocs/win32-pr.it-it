---
description: 'Altre informazioni su: CimMofDeserializer. OnClassNeeded delegate (String, String, String)'
title: Delegato CimMofDeserializer.OnClassNeeded (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.OnClassNeeded delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::OnClassNeeded
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 50e107c09eccde03446278516a1f125f4ad86022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308850"
---
# <a name="cimmofdeserializeronclassneeded-delegate-string-string-string"></a>Delegato CimMofDeserializer. OnClassNeeded (String, String, String)

Rappresenta un callback per recuperare una classe CIM per il server, lo spazio dei nomi e il nome della classe specificati.

**Spazio dei nomi:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintassi

``` csharp
public delegate CimClass OnClassNeeded(
    string serverName,
    string namespaceName,
    string className
)
```

``` c++
public delegate CimClass^ OnClassNeeded(
    String^ serverName,
    String^ namespaceName,
    String^ className
)
```

``` fsharp
type OnClassNeeded = 
    delegate of 
        serverName:string *
        namespaceName:string *
        className:string -> CimClass
```

``` vb
Public Delegate Function OnClassNeeded (
    serverName As String,
    namespaceName As String,
    className As String,
) As CimClass
```

#### <a name="parameters"></a>Parametri

  - serverName  
    Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Nome del server per la classe CIM.

<!-- end list -->

  - namespaceName  
    Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Nome dello spazio dei nomi per la classe CIM.

<!-- end list -->

  - className  
    Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Nome della classe per la classe CIM.

#### <a name="return-value"></a>Valore restituito

Tipo: [classe CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))

Restituisce la classe CIM corrispondente agli argomenti specificati oppure **null** se la classe non viene trovata.

## <a name="see-also"></a>Vedere anche

[Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
