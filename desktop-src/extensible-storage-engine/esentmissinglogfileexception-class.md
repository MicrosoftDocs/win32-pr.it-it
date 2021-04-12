---
description: 'Altre informazioni su: classe EsentMissingLogFileException'
title: Classe EsentMissingLogFileException
TOCTitle: EsentMissingLogFileException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingLogFileException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissinglogfileexception(v=EXCHG.10)
ms:contentKeyID: 55102306
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingLogFileException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingLogFileException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6f926e25f8999dabdc282342a3f071753241578
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130879"
---
# <a name="esentmissinglogfileexception-class"></a><span data-ttu-id="5a517-103">Classe EsentMissingLogFileException</span><span class="sxs-lookup"><span data-stu-id="5a517-103">EsentMissingLogFileException class</span></span>

<span data-ttu-id="5a517-104">Classe di base per JET_err. Eccezioni MissingLogFile.</span><span class="sxs-lookup"><span data-stu-id="5a517-104">Base class for JET_err.MissingLogFile exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5a517-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="5a517-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5a517-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5a517-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5a517-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="5a517-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5a517-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="5a517-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5a517-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="5a517-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5a517-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="5a517-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="5a517-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="5a517-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="5a517-112">Microsoft. ISAM. esent. Interop. EsentMissingLogFileException</span><span class="sxs-lookup"><span data-stu-id="5a517-112">Microsoft.Isam.Esent.Interop.EsentMissingLogFileException</span></span>  

<span data-ttu-id="5a517-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5a517-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5a517-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5a517-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5a517-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5a517-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingLogFileException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentMissingLogFileException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingLogFileException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="5a517-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="5a517-116">Thread safety</span></span>

<span data-ttu-id="5a517-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="5a517-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5a517-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="5a517-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5a517-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5a517-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5a517-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5a517-120">Reference</span></span>

[<span data-ttu-id="5a517-121">Membri di EsentMissingLogFileException</span><span class="sxs-lookup"><span data-stu-id="5a517-121">EsentMissingLogFileException members</span></span>](./esentmissinglogfileexception-members.md)

[<span data-ttu-id="5a517-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5a517-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
