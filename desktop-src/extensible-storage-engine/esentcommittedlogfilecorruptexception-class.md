---
description: 'Altre informazioni su: classe EsentCommittedLogFileCorruptException'
title: Classe EsentCommittedLogFileCorruptException
TOCTitle: EsentCommittedLogFileCorruptException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcommittedlogfilecorruptexception(v=EXCHG.10)
ms:contentKeyID: 55101273
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbc9d9342da650838aca4a291cc0196bc40fc77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305816"
---
# <a name="esentcommittedlogfilecorruptexception-class"></a><span data-ttu-id="7d05e-103">Classe EsentCommittedLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="7d05e-103">EsentCommittedLogFileCorruptException class</span></span>

<span data-ttu-id="7d05e-104">Classe base per le eccezioni JET_err. CommittedLogFileCorrupt.</span><span class="sxs-lookup"><span data-stu-id="7d05e-104">Base class for JET_err.CommittedLogFileCorrupt exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="7d05e-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="7d05e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="7d05e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="7d05e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="7d05e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="7d05e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="7d05e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="7d05e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="7d05e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="7d05e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="7d05e-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="7d05e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="7d05e-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="7d05e-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="7d05e-112">Microsoft. ISAM. esent. Interop. EsentCommittedLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="7d05e-112">Microsoft.Isam.Esent.Interop.EsentCommittedLogFileCorruptException</span></span>  

<span data-ttu-id="7d05e-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7d05e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7d05e-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7d05e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7d05e-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7d05e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCommittedLogFileCorruptException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentCommittedLogFileCorruptException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCommittedLogFileCorruptException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="7d05e-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="7d05e-116">Thread safety</span></span>

<span data-ttu-id="7d05e-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7d05e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="7d05e-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7d05e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d05e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7d05e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7d05e-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7d05e-120">Reference</span></span>

[<span data-ttu-id="7d05e-121">Membri di EsentCommittedLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="7d05e-121">EsentCommittedLogFileCorruptException members</span></span>](./esentcommittedlogfilecorruptexception-members.md)

[<span data-ttu-id="7d05e-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7d05e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
