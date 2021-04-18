---
description: 'Altre informazioni su: classe EsentTooManyKeysException'
title: Classe EsentTooManyKeysException
TOCTitle: EsentTooManyKeysException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyKeysException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanykeysexception(v=EXCHG.10)
ms:contentKeyID: 55103066
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyKeysException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyKeysException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d90152c0d811566681599033ffc950d1f880cc2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317423"
---
# <a name="esenttoomanykeysexception-class"></a><span data-ttu-id="97343-103">Classe EsentTooManyKeysException</span><span class="sxs-lookup"><span data-stu-id="97343-103">EsentTooManyKeysException class</span></span>

<span data-ttu-id="97343-104">Classe di base per JET_err. Eccezioni TooManyKeys.</span><span class="sxs-lookup"><span data-stu-id="97343-104">Base class for JET_err.TooManyKeys exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="97343-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="97343-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="97343-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="97343-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="97343-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="97343-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="97343-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="97343-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="97343-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="97343-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="97343-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="97343-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="97343-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="97343-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="97343-112">Microsoft. ISAM. esent. Interop. EsentTooManyKeysException</span><span class="sxs-lookup"><span data-stu-id="97343-112">Microsoft.Isam.Esent.Interop.EsentTooManyKeysException</span></span>  

<span data-ttu-id="97343-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="97343-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="97343-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="97343-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="97343-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97343-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyKeysException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyKeysException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyKeysException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="97343-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="97343-116">Thread safety</span></span>

<span data-ttu-id="97343-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="97343-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="97343-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="97343-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="97343-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97343-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="97343-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="97343-120">Reference</span></span>

[<span data-ttu-id="97343-121">Membri di EsentTooManyKeysException</span><span class="sxs-lookup"><span data-stu-id="97343-121">EsentTooManyKeysException members</span></span>](./esenttoomanykeysexception-members.md)

[<span data-ttu-id="97343-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="97343-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
