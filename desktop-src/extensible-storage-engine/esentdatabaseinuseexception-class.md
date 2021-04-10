---
description: 'Altre informazioni su: classe EsentDatabaseInUseException'
title: Classe EsentDatabaseInUseException
TOCTitle: EsentDatabaseInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseinuseexception(v=EXCHG.10)
ms:contentKeyID: 55101372
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8b97ce4cc0a02b322a0abfc882ee0fce398fb04b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879422"
---
# <a name="esentdatabaseinuseexception-class"></a><span data-ttu-id="355a2-103">Classe EsentDatabaseInUseException</span><span class="sxs-lookup"><span data-stu-id="355a2-103">EsentDatabaseInUseException class</span></span>

<span data-ttu-id="355a2-104">Classe di base per JET_err. Eccezioni DatabaseInUse.</span><span class="sxs-lookup"><span data-stu-id="355a2-104">Base class for JET_err.DatabaseInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="355a2-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="355a2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="355a2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="355a2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="355a2-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="355a2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="355a2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="355a2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="355a2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="355a2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="355a2-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="355a2-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="355a2-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="355a2-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="355a2-112">Microsoft. ISAM. esent. Interop. EsentDatabaseInUseException</span><span class="sxs-lookup"><span data-stu-id="355a2-112">Microsoft.Isam.Esent.Interop.EsentDatabaseInUseException</span></span>  

<span data-ttu-id="355a2-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="355a2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="355a2-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="355a2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="355a2-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="355a2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentDatabaseInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseInUseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="355a2-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="355a2-116">Thread safety</span></span>

<span data-ttu-id="355a2-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="355a2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="355a2-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="355a2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="355a2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="355a2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="355a2-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="355a2-120">Reference</span></span>

[<span data-ttu-id="355a2-121">Membri di EsentDatabaseInUseException</span><span class="sxs-lookup"><span data-stu-id="355a2-121">EsentDatabaseInUseException members</span></span>](./esentdatabaseinuseexception-members.md)

[<span data-ttu-id="355a2-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="355a2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
