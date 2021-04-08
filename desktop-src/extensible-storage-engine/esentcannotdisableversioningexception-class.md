---
description: 'Altre informazioni su: classe EsentCannotDisableVersioningException'
title: Classe EsentCannotDisableVersioningException
TOCTitle: EsentCannotDisableVersioningException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcannotdisableversioningexception(v=EXCHG.10)
ms:contentKeyID: 55101260
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df332b292d3bee2c4e25d9fc331d53f67bf9a0ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749402"
---
# <a name="esentcannotdisableversioningexception-class"></a><span data-ttu-id="5d156-103">Classe EsentCannotDisableVersioningException</span><span class="sxs-lookup"><span data-stu-id="5d156-103">EsentCannotDisableVersioningException class</span></span>

<span data-ttu-id="5d156-104">Classe di base per JET_err. Eccezioni CannotDisableVersioning.</span><span class="sxs-lookup"><span data-stu-id="5d156-104">Base class for JET_err.CannotDisableVersioning exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="5d156-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="5d156-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="5d156-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="5d156-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="5d156-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="5d156-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="5d156-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="5d156-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="5d156-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="5d156-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="5d156-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="5d156-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="5d156-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="5d156-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="5d156-112">Microsoft. ISAM. esent. Interop. EsentCannotDisableVersioningException</span><span class="sxs-lookup"><span data-stu-id="5d156-112">Microsoft.Isam.Esent.Interop.EsentCannotDisableVersioningException</span></span>  

<span data-ttu-id="5d156-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5d156-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5d156-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5d156-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5d156-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d156-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentCannotDisableVersioningException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentCannotDisableVersioningException
```

``` csharp
[SerializableAttribute]
public sealed class EsentCannotDisableVersioningException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="5d156-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="5d156-116">Thread safety</span></span>

<span data-ttu-id="5d156-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="5d156-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="5d156-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="5d156-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d156-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5d156-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5d156-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5d156-120">Reference</span></span>

[<span data-ttu-id="5d156-121">Membri di EsentCannotDisableVersioningException</span><span class="sxs-lookup"><span data-stu-id="5d156-121">EsentCannotDisableVersioningException members</span></span>](./esentcannotdisableversioningexception-members.md)

[<span data-ttu-id="5d156-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5d156-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
