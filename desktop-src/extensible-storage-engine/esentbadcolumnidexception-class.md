---
description: 'Altre informazioni su: classe EsentBadColumnIdException'
title: Classe EsentBadColumnIdException
TOCTitle: EsentBadColumnIdException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadColumnIdException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbadcolumnidexception(v=EXCHG.10)
ms:contentKeyID: 55101061
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadColumnIdException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadColumnIdException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 94b7e898b95130df4a1f7e3a88fa2e450d3b6776
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058008"
---
# <a name="esentbadcolumnidexception-class"></a><span data-ttu-id="b4b8a-103">Classe EsentBadColumnIdException</span><span class="sxs-lookup"><span data-stu-id="b4b8a-103">EsentBadColumnIdException class</span></span>

<span data-ttu-id="b4b8a-104">Classe di base per JET_err. Eccezioni BadColumnId.</span><span class="sxs-lookup"><span data-stu-id="b4b8a-104">Base class for JET_err.BadColumnId exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b4b8a-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="b4b8a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b4b8a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b4b8a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b4b8a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b4b8a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b4b8a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b4b8a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b4b8a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b4b8a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b4b8a-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b4b8a-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b4b8a-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="b4b8a-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b4b8a-112">Microsoft. ISAM. esent. Interop. EsentBadColumnIdException</span><span class="sxs-lookup"><span data-stu-id="b4b8a-112">Microsoft.Isam.Esent.Interop.EsentBadColumnIdException</span></span>  

<span data-ttu-id="b4b8a-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4b8a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4b8a-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4b8a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b8a-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4b8a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadColumnIdException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentBadColumnIdException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadColumnIdException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b4b8a-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="b4b8a-116">Thread safety</span></span>

<span data-ttu-id="b4b8a-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b4b8a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b4b8a-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b4b8a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4b8a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4b8a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4b8a-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b4b8a-120">Reference</span></span>

[<span data-ttu-id="b4b8a-121">Membri di EsentBadColumnIdException</span><span class="sxs-lookup"><span data-stu-id="b4b8a-121">EsentBadColumnIdException members</span></span>](./esentbadcolumnidexception-members.md)

[<span data-ttu-id="b4b8a-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b4b8a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
