---
description: 'Altre informazioni su: classe EsentOutOfDatabaseSpaceException'
title: Classe EsentOutOfDatabaseSpaceException
TOCTitle: EsentOutOfDatabaseSpaceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofdatabasespaceexception(v=EXCHG.10)
ms:contentKeyID: 55102410
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ece3a81fa0687299edba0857b15f4c0abc50e403
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310869"
---
# <a name="esentoutofdatabasespaceexception-class"></a><span data-ttu-id="48762-103">Classe EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="48762-103">EsentOutOfDatabaseSpaceException class</span></span>

<span data-ttu-id="48762-104">Classe di base per JET_err. Eccezioni OutOfDatabaseSpace.</span><span class="sxs-lookup"><span data-stu-id="48762-104">Base class for JET_err.OutOfDatabaseSpace exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="48762-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="48762-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="48762-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="48762-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="48762-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="48762-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="48762-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="48762-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="48762-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="48762-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="48762-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="48762-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="48762-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="48762-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="48762-112">Microsoft. ISAM. esent. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="48762-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="48762-113">Microsoft. ISAM. esent. Interop. EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="48762-113">Microsoft.Isam.Esent.Interop.EsentOutOfDatabaseSpaceException</span></span>  

<span data-ttu-id="48762-114">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="48762-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="48762-115">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="48762-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="48762-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="48762-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfDatabaseSpaceException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentOutOfDatabaseSpaceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfDatabaseSpaceException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="48762-117">Thread safety</span><span class="sxs-lookup"><span data-stu-id="48762-117">Thread safety</span></span>

<span data-ttu-id="48762-118">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="48762-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="48762-119">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="48762-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="48762-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="48762-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="48762-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="48762-121">Reference</span></span>

[<span data-ttu-id="48762-122">Membri di EsentOutOfDatabaseSpaceException</span><span class="sxs-lookup"><span data-stu-id="48762-122">EsentOutOfDatabaseSpaceException members</span></span>](./esentoutofdatabasespaceexception-members.md)

[<span data-ttu-id="48762-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="48762-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
