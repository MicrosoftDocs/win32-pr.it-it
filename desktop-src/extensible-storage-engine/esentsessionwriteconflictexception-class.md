---
description: 'Altre informazioni su: classe EsentSessionWriteConflictException'
title: Classe EsentSessionWriteConflictException
TOCTitle: EsentSessionWriteConflictException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessionwriteconflictexception(v=EXCHG.10)
ms:contentKeyID: 55107337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0725bc2d1215e4e71e0e68b2fa7e0d4246a96b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885618"
---
# <a name="esentsessionwriteconflictexception-class"></a><span data-ttu-id="0424f-103">Classe EsentSessionWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="0424f-103">EsentSessionWriteConflictException class</span></span>

<span data-ttu-id="0424f-104">Classe di base per JET_err. Eccezioni SessionWriteConflict.</span><span class="sxs-lookup"><span data-stu-id="0424f-104">Base class for JET_err.SessionWriteConflict exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0424f-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="0424f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0424f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0424f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0424f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0424f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0424f-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0424f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="0424f-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0424f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="0424f-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="0424f-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="0424f-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="0424f-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="0424f-112">Microsoft. ISAM. esent. Interop. EsentSessionWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="0424f-112">Microsoft.Isam.Esent.Interop.EsentSessionWriteConflictException</span></span>  

<span data-ttu-id="0424f-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0424f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0424f-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0424f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0424f-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0424f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionWriteConflictException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionWriteConflictException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionWriteConflictException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="0424f-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="0424f-116">Thread safety</span></span>

<span data-ttu-id="0424f-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0424f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0424f-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0424f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0424f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0424f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0424f-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0424f-120">Reference</span></span>

[<span data-ttu-id="0424f-121">Membri di EsentSessionWriteConflictException</span><span class="sxs-lookup"><span data-stu-id="0424f-121">EsentSessionWriteConflictException members</span></span>](./esentsessionwriteconflictexception-members.md)

[<span data-ttu-id="0424f-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0424f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
