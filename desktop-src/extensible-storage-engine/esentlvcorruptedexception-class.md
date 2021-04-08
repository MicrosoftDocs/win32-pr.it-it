---
description: 'Altre informazioni su: classe EsentLVCorruptedException'
title: Classe EsentLVCorruptedException
TOCTitle: EsentLVCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLVCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlvcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102240
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLVCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLVCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b075aa72b7ddbece409ab49e4e36bea86489de1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880989"
---
# <a name="esentlvcorruptedexception-class"></a><span data-ttu-id="02845-103">Classe EsentLVCorruptedException</span><span class="sxs-lookup"><span data-stu-id="02845-103">EsentLVCorruptedException class</span></span>

<span data-ttu-id="02845-104">Classe di base per JET_err. Eccezioni LVCorrupted.</span><span class="sxs-lookup"><span data-stu-id="02845-104">Base class for JET_err.LVCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="02845-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="02845-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="02845-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="02845-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="02845-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="02845-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="02845-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="02845-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="02845-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="02845-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="02845-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="02845-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="02845-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="02845-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="02845-112">Microsoft. ISAM. esent. Interop. EsentLVCorruptedException</span><span class="sxs-lookup"><span data-stu-id="02845-112">Microsoft.Isam.Esent.Interop.EsentLVCorruptedException</span></span>  

<span data-ttu-id="02845-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="02845-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="02845-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="02845-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="02845-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02845-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLVCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLVCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLVCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="02845-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="02845-116">Thread safety</span></span>

<span data-ttu-id="02845-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="02845-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="02845-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="02845-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="02845-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02845-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="02845-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="02845-120">Reference</span></span>

[<span data-ttu-id="02845-121">Membri di EsentLVCorruptedException</span><span class="sxs-lookup"><span data-stu-id="02845-121">EsentLVCorruptedException members</span></span>](./esentlvcorruptedexception-members.md)

[<span data-ttu-id="02845-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="02845-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
