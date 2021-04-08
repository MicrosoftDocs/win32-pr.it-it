---
description: 'Altre informazioni su: classe EsentRequiredLogFilesMissingException'
title: Classe EsentRequiredLogFilesMissingException
TOCTitle: EsentRequiredLogFilesMissingException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrequiredlogfilesmissingexception(v=EXCHG.10)
ms:contentKeyID: 55102617
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c2ac90c685daa306d260c5386bae4e988d6d25a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049403"
---
# <a name="esentrequiredlogfilesmissingexception-class"></a><span data-ttu-id="7be4e-103">Classe EsentRequiredLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="7be4e-103">EsentRequiredLogFilesMissingException class</span></span>

<span data-ttu-id="7be4e-104">Classe di base per JET_err. Eccezioni RequiredLogFilesMissing.</span><span class="sxs-lookup"><span data-stu-id="7be4e-104">Base class for JET_err.RequiredLogFilesMissing exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7be4e-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="7be4e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7be4e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7be4e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7be4e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7be4e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7be4e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="7be4e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7be4e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="7be4e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7be4e-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="7be4e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="7be4e-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="7be4e-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="7be4e-112">Microsoft. ISAM. esent. Interop. EsentRequiredLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="7be4e-112">Microsoft.Isam.Esent.Interop.EsentRequiredLogFilesMissingException</span></span>  

<span data-ttu-id="7be4e-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7be4e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7be4e-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7be4e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7be4e-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7be4e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRequiredLogFilesMissingException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentRequiredLogFilesMissingException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRequiredLogFilesMissingException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="7be4e-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="7be4e-116">Thread safety</span></span>

<span data-ttu-id="7be4e-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7be4e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7be4e-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7be4e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7be4e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7be4e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7be4e-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7be4e-120">Reference</span></span>

[<span data-ttu-id="7be4e-121">Membri di EsentRequiredLogFilesMissingException</span><span class="sxs-lookup"><span data-stu-id="7be4e-121">EsentRequiredLogFilesMissingException members</span></span>](./esentrequiredlogfilesmissingexception-members.md)

[<span data-ttu-id="7be4e-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7be4e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
