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
# <a name="cimmofdeserializergetincludedfilecontent-delegate-string"></a><span data-ttu-id="574c7-103">Delegato CimMofDeserializer. GetIncludedFileContent (String)</span><span class="sxs-lookup"><span data-stu-id="574c7-103">CimMofDeserializer.GetIncludedFileContent delegate (String)</span></span>

<span data-ttu-id="574c7-104">Rappresenta un callback per recuperare il contenuto del file sotto forma di matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="574c7-104">Represents a callback to retrieve the file's contents in the form of a byte array.</span></span>

<span data-ttu-id="574c7-105">**Spazio dei nomi:**   [Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="574c7-105">**Namespace:**   [Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>  
<span data-ttu-id="574c7-106">**Assembly:**  Microsoft. Management. Infrastructure (in Microsoft.Management.Infrastructure.dll)</span><span class="sxs-lookup"><span data-stu-id="574c7-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="574c7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="574c7-107">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="574c7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="574c7-108">Parameters</span></span>

  - <span data-ttu-id="574c7-109">fileName</span><span class="sxs-lookup"><span data-stu-id="574c7-109">fileName</span></span>  
    <span data-ttu-id="574c7-110">Tipo: [System. String](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="574c7-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="574c7-111">Nome file, incluso il percorso.</span><span class="sxs-lookup"><span data-stu-id="574c7-111">File name, including path.</span></span>

#### <a name="return-value"></a><span data-ttu-id="574c7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="574c7-112">Return Value</span></span>

<span data-ttu-id="574c7-113">Tipo: [System. byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span><span class="sxs-lookup"><span data-stu-id="574c7-113">Type: [System.Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]</span></span>

<span data-ttu-id="574c7-114">Restituisce il contenuto del file sotto forma di matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="574c7-114">Returns the file's contents in the form of a byte array.</span></span>

## <a name="see-also"></a><span data-ttu-id="574c7-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="574c7-115">See Also</span></span>

<span data-ttu-id="574c7-116">[Microsoft. Management. Infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="574c7-116">[Microsoft.Management.Infrastructure.Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))</span></span>
