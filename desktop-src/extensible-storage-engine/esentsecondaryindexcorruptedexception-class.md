---
description: 'Altre informazioni su: classe EsentSecondaryIndexCorruptedException'
title: Classe EsentSecondaryIndexCorruptedException
TOCTitle: EsentSecondaryIndexCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsecondaryindexcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102677
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af6cc22e45db383dc3e5fd83b125263d055b95c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318746"
---
# <a name="esentsecondaryindexcorruptedexception-class"></a><span data-ttu-id="0f279-103">Classe EsentSecondaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0f279-103">EsentSecondaryIndexCorruptedException class</span></span>

<span data-ttu-id="0f279-104">Classe di base per JET_err. Eccezioni SecondaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="0f279-104">Base class for JET_err.SecondaryIndexCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0f279-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="0f279-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0f279-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0f279-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0f279-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0f279-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0f279-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0f279-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0f279-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0f279-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0f279-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0f279-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="0f279-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="0f279-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="0f279-112">Microsoft. ISAM. esent. Interop. EsentSecondaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0f279-112">Microsoft.Isam.Esent.Interop.EsentSecondaryIndexCorruptedException</span></span>  

<span data-ttu-id="0f279-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0f279-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0f279-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0f279-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0f279-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f279-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSecondaryIndexCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentSecondaryIndexCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSecondaryIndexCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="0f279-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="0f279-116">Thread safety</span></span>

<span data-ttu-id="0f279-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0f279-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0f279-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0f279-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0f279-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f279-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0f279-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0f279-120">Reference</span></span>

[<span data-ttu-id="0f279-121">Membri di EsentSecondaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="0f279-121">EsentSecondaryIndexCorruptedException members</span></span>](./esentsecondaryindexcorruptedexception-members.md)

[<span data-ttu-id="0f279-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0f279-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
