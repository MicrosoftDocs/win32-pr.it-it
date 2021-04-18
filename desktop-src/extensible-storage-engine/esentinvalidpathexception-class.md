---
description: 'Altre informazioni su: classe EsentInvalidPathException'
title: Classe EsentInvalidPathException
TOCTitle: EsentInvalidPathException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidPathException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidpathexception(v=EXCHG.10)
ms:contentKeyID: 55102012
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidPathException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidPathException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4b648cd28a5a0dc52c1418b0b695f4645d954371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318765"
---
# <a name="esentinvalidpathexception-class"></a><span data-ttu-id="a1b43-103">Classe EsentInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="a1b43-103">EsentInvalidPathException class</span></span>

<span data-ttu-id="a1b43-104">Classe di base per JET_err. Eccezioni InvalidPath.</span><span class="sxs-lookup"><span data-stu-id="a1b43-104">Base class for JET_err.InvalidPath exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a1b43-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="a1b43-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a1b43-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a1b43-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a1b43-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a1b43-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a1b43-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a1b43-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a1b43-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a1b43-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a1b43-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a1b43-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a1b43-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="a1b43-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a1b43-112">Microsoft. ISAM. esent. Interop. EsentInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="a1b43-112">Microsoft.Isam.Esent.Interop.EsentInvalidPathException</span></span>  

<span data-ttu-id="a1b43-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a1b43-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a1b43-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a1b43-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a1b43-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1b43-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidPathException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentInvalidPathException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidPathException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a1b43-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="a1b43-116">Thread safety</span></span>

<span data-ttu-id="a1b43-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a1b43-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a1b43-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a1b43-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1b43-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1b43-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a1b43-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a1b43-120">Reference</span></span>

[<span data-ttu-id="a1b43-121">Membri di EsentInvalidPathException</span><span class="sxs-lookup"><span data-stu-id="a1b43-121">EsentInvalidPathException members</span></span>](./esentinvalidpathexception-members.md)

[<span data-ttu-id="a1b43-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a1b43-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
