---
description: 'Altre informazioni su: classe EsentKeyTruncatedException'
title: Classe EsentKeyTruncatedException
TOCTitle: EsentKeyTruncatedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentkeytruncatedexception(v=EXCHG.10)
ms:contentKeyID: 55102126
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ba38f11d6e78383bb313a9ae798b79efb2bfd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318762"
---
# <a name="esentkeytruncatedexception-class"></a><span data-ttu-id="55439-103">Classe EsentKeyTruncatedException</span><span class="sxs-lookup"><span data-stu-id="55439-103">EsentKeyTruncatedException class</span></span>

<span data-ttu-id="55439-104">Classe di base per JET_err. Eccezioni troncate.</span><span class="sxs-lookup"><span data-stu-id="55439-104">Base class for JET_err.KeyTruncated exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="55439-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="55439-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="55439-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="55439-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="55439-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="55439-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="55439-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="55439-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="55439-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="55439-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="55439-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="55439-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="55439-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="55439-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="55439-112">Microsoft. ISAM. esent. Interop. EsentKeyTruncatedException</span><span class="sxs-lookup"><span data-stu-id="55439-112">Microsoft.Isam.Esent.Interop.EsentKeyTruncatedException</span></span>  

<span data-ttu-id="55439-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="55439-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="55439-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="55439-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="55439-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="55439-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentKeyTruncatedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentKeyTruncatedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentKeyTruncatedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="55439-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="55439-116">Thread safety</span></span>

<span data-ttu-id="55439-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="55439-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="55439-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="55439-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="55439-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="55439-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="55439-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="55439-120">Reference</span></span>

[<span data-ttu-id="55439-121">Membri di EsentKeyTruncatedException</span><span class="sxs-lookup"><span data-stu-id="55439-121">EsentKeyTruncatedException members</span></span>](./esentkeytruncatedexception-members.md)

[<span data-ttu-id="55439-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="55439-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
