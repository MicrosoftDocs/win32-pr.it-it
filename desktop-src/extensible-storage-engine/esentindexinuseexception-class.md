---
description: 'Altre informazioni su: classe EsentIndexInUseException'
title: Classe EsentIndexInUseException
TOCTitle: EsentIndexInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentIndexInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentindexinuseexception(v=EXCHG.10)
ms:contentKeyID: 55101815
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentIndexInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentIndexInUseException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7b9460bcc2d9ca0ce8676c358781c59d881a5ea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308057"
---
# <a name="esentindexinuseexception-class"></a><span data-ttu-id="a5b8c-103">Classe EsentIndexInUseException</span><span class="sxs-lookup"><span data-stu-id="a5b8c-103">EsentIndexInUseException class</span></span>

<span data-ttu-id="a5b8c-104">Classe di base per JET_err. Eccezioni IndexInUse.</span><span class="sxs-lookup"><span data-stu-id="a5b8c-104">Base class for JET_err.IndexInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a5b8c-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="a5b8c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a5b8c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a5b8c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a5b8c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a5b8c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a5b8c-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a5b8c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a5b8c-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a5b8c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a5b8c-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a5b8c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a5b8c-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="a5b8c-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="a5b8c-112">Microsoft. ISAM. esent. Interop. EsentIndexInUseException</span><span class="sxs-lookup"><span data-stu-id="a5b8c-112">Microsoft.Isam.Esent.Interop.EsentIndexInUseException</span></span>  

<span data-ttu-id="a5b8c-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a5b8c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a5b8c-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a5b8c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b8c-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5b8c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentIndexInUseException _
    Inherits EsentStateException
'Usage
Dim instance As EsentIndexInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentIndexInUseException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="a5b8c-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="a5b8c-116">Thread safety</span></span>

<span data-ttu-id="a5b8c-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a5b8c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a5b8c-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a5b8c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5b8c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5b8c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a5b8c-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a5b8c-120">Reference</span></span>

[<span data-ttu-id="a5b8c-121">Membri di EsentIndexInUseException</span><span class="sxs-lookup"><span data-stu-id="a5b8c-121">EsentIndexInUseException members</span></span>](./esentindexinuseexception-members.md)

[<span data-ttu-id="a5b8c-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a5b8c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
