---
description: 'Altre informazioni su: classe EsentInvalidInstanceException'
title: Classe EsentInvalidInstanceException
TOCTitle: EsentInvalidInstanceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidinstanceexception(v=EXCHG.10)
ms:contentKeyID: 55101939
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ba855e89f7714b7042b882b5c8cb28eba3dca3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233096"
---
# <a name="esentinvalidinstanceexception-class"></a><span data-ttu-id="cbe16-103">Classe EsentInvalidInstanceException</span><span class="sxs-lookup"><span data-stu-id="cbe16-103">EsentInvalidInstanceException class</span></span>

<span data-ttu-id="cbe16-104">Classe di base per JET_err. Eccezioni InvalidInstance.</span><span class="sxs-lookup"><span data-stu-id="cbe16-104">Base class for JET_err.InvalidInstance exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="cbe16-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="cbe16-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="cbe16-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="cbe16-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="cbe16-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="cbe16-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="cbe16-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="cbe16-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="cbe16-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="cbe16-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="cbe16-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="cbe16-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="cbe16-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="cbe16-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="cbe16-112">Microsoft. ISAM. esent. Interop. EsentInvalidInstanceException</span><span class="sxs-lookup"><span data-stu-id="cbe16-112">Microsoft.Isam.Esent.Interop.EsentInvalidInstanceException</span></span>  

<span data-ttu-id="cbe16-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cbe16-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cbe16-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cbe16-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cbe16-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cbe16-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidInstanceException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidInstanceException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidInstanceException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="cbe16-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="cbe16-116">Thread safety</span></span>

<span data-ttu-id="cbe16-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="cbe16-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="cbe16-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="cbe16-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbe16-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cbe16-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cbe16-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="cbe16-120">Reference</span></span>

[<span data-ttu-id="cbe16-121">Membri di EsentInvalidInstanceException</span><span class="sxs-lookup"><span data-stu-id="cbe16-121">EsentInvalidInstanceException members</span></span>](./esentinvalidinstanceexception-members.md)

[<span data-ttu-id="cbe16-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cbe16-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
