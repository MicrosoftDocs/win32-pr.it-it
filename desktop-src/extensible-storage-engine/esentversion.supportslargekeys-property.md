---
description: 'Altre informazioni su: Proprietà EsentVersion. SupportsLargeKeys'
title: Proprietà EsentVersion. SupportsLargeKeys
TOCTitle: 'SupportsLargeKeys property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentversion.supportslargekeys(v=EXCHG.10)
ms:contentKeyID: 55103180
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentVersion.SupportsLargeKeys
- Microsoft.Isam.Esent.Interop.EsentVersion.get_SupportsLargeKeys
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43ee88b7c0e190d9c717c087deeb5fc4556e6575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319704"
---
# <a name="esentversionsupportslargekeys-property"></a><span data-ttu-id="89162-103">Proprietà EsentVersion. SupportsLargeKeys</span><span class="sxs-lookup"><span data-stu-id="89162-103">EsentVersion.SupportsLargeKeys property</span></span>

<span data-ttu-id="89162-104">Ottiene un valore che indica se \> sono supportate le chiavi Large (255 byte).</span><span class="sxs-lookup"><span data-stu-id="89162-104">Gets a value that indicates whether large (\> 255 byte) keys are supported.</span></span> <span data-ttu-id="89162-105">È possibile specificare le dimensioni della chiave per un indice nell'oggetto [JET_INDEXCREATE](./jet-indexcreate-class.md) .</span><span class="sxs-lookup"><span data-stu-id="89162-105">The key size for an index can be specified in the [JET_INDEXCREATE](./jet-indexcreate-class.md) object.</span></span>

<span data-ttu-id="89162-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89162-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89162-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89162-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89162-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89162-108">Syntax</span></span>

``` vb
'Declaration
Public Shared ReadOnly Property SupportsLargeKeys As Boolean
    Get
'Usage
Dim value As Boolean

value = EsentVersion.SupportsLargeKeys
```

``` csharp
public static bool SupportsLargeKeys { get; }
```

#### <a name="property-value"></a><span data-ttu-id="89162-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="89162-109">Property value</span></span>

<span data-ttu-id="89162-110">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="89162-110">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="89162-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89162-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89162-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="89162-112">Reference</span></span>

[<span data-ttu-id="89162-113">Classe EsentVersion</span><span class="sxs-lookup"><span data-stu-id="89162-113">EsentVersion class</span></span>](./esentversion-class.md)

[<span data-ttu-id="89162-114">Membri di EsentVersion</span><span class="sxs-lookup"><span data-stu-id="89162-114">EsentVersion members</span></span>](./esentversion-members.md)

[<span data-ttu-id="89162-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="89162-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
