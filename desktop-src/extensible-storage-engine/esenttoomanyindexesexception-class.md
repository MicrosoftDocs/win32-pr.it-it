---
description: 'Altre informazioni su: classe EsentTooManyIndexesException'
title: Classe EsentTooManyIndexesException
TOCTitle: EsentTooManyIndexesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyindexesexception(v=EXCHG.10)
ms:contentKeyID: 55103060
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a1d895f61b3ad1f25b8992b43da1fd14f29f22a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316518"
---
# <a name="esenttoomanyindexesexception-class"></a><span data-ttu-id="19352-103">Classe EsentTooManyIndexesException</span><span class="sxs-lookup"><span data-stu-id="19352-103">EsentTooManyIndexesException class</span></span>

<span data-ttu-id="19352-104">Classe di base per JET_err. Eccezioni TooManyIndexes.</span><span class="sxs-lookup"><span data-stu-id="19352-104">Base class for JET_err.TooManyIndexes exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="19352-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="19352-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="19352-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="19352-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="19352-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="19352-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="19352-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="19352-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="19352-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="19352-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="19352-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="19352-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="19352-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="19352-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="19352-112">Microsoft. ISAM. esent. Interop. EsentTooManyIndexesException</span><span class="sxs-lookup"><span data-stu-id="19352-112">Microsoft.Isam.Esent.Interop.EsentTooManyIndexesException</span></span>  

<span data-ttu-id="19352-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="19352-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="19352-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="19352-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="19352-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19352-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyIndexesException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyIndexesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyIndexesException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="19352-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="19352-116">Thread safety</span></span>

<span data-ttu-id="19352-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="19352-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="19352-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="19352-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="19352-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19352-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="19352-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="19352-120">Reference</span></span>

[<span data-ttu-id="19352-121">Membri di EsentTooManyIndexesException</span><span class="sxs-lookup"><span data-stu-id="19352-121">EsentTooManyIndexesException members</span></span>](./esenttoomanyindexesexception-members.md)

[<span data-ttu-id="19352-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="19352-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
