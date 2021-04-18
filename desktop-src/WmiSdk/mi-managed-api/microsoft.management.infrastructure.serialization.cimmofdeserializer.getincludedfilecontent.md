---
description: 'Altre informazioni su: CimMofDeserializer. GetIncludedFileContent delegate (String)'
title: Delegato CimMofDeserializer. GetIncludedFileContent (Microsoft. Management. Infrastructure. Serialization)
TOCTitle: CimMofDeserializer.GetIncludedFileContent delegate (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: T:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft::Management::Infrastructure::Serialization::CimMofDeserializer::GetIncludedFileContent
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent..ctor
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.BeginInvoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.Invoke
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent.EndInvoke
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: cb922d785da7d01de93adec56cefee29785210d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308851"
---
# <a name="cimmofdeserializergetincludedfilecontent-delegate-string"></a>Delegato CimMofDeserializer. GetIncludedFileContent (String)

Rappresenta un callback per recuperare il contenuto del file sotto forma di matrice di byte.

**Spazio dei nomi:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Sintassi

``` csharp
public delegate byte[] GetIncludedFileContent(
    string fileName
)
```

``` c++
public delegate array<unsigned char>^ GetIncludedFileContent(
    String^ fileName
)
```

``` fsharp
type GetIncludedFileContent = 
    delegate of 
        fileName:string -> byte[]
```

``` vb
Public Delegate Function GetIncludedFileContent (
    fileName As String
) As Byte()
```

#### <a name="parameters"></a>Parametri

  - fileName  
    Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Nome file, incluso il percorso.

#### <a name="return-value"></a>Valore restituito

Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]

Restituisce il contenuto del file sotto forma di matrice di byte.

## <a name="see-also"></a>Vedere anche

[Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
