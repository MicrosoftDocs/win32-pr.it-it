---
description: 'Altre informazioni su: classe EsentTooManyColumnsException'
title: Classe EsentTooManyColumnsException
TOCTitle: EsentTooManyColumnsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanycolumnsexception(v=EXCHG.10)
ms:contentKeyID: 55103051
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2191abd07aea85dac6275f3c42f34acd13376035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317427"
---
# <a name="esenttoomanycolumnsexception-class"></a><span data-ttu-id="dae6b-103">Classe EsentTooManyColumnsException</span><span class="sxs-lookup"><span data-stu-id="dae6b-103">EsentTooManyColumnsException class</span></span>

<span data-ttu-id="dae6b-104">Classe di base per JET_err. Eccezioni TooManyColumns.</span><span class="sxs-lookup"><span data-stu-id="dae6b-104">Base class for JET_err.TooManyColumns exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="dae6b-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="dae6b-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="dae6b-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="dae6b-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="dae6b-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="dae6b-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="dae6b-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="dae6b-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="dae6b-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="dae6b-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="dae6b-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="dae6b-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="dae6b-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="dae6b-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="dae6b-112">Microsoft. ISAM. esent. Interop. EsentTooManyColumnsException</span><span class="sxs-lookup"><span data-stu-id="dae6b-112">Microsoft.Isam.Esent.Interop.EsentTooManyColumnsException</span></span>  

<span data-ttu-id="dae6b-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="dae6b-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="dae6b-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="dae6b-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="dae6b-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dae6b-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyColumnsException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTooManyColumnsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyColumnsException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="dae6b-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="dae6b-116">Thread safety</span></span>

<span data-ttu-id="dae6b-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="dae6b-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="dae6b-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="dae6b-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="dae6b-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dae6b-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="dae6b-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="dae6b-120">Reference</span></span>

[<span data-ttu-id="dae6b-121">Membri di EsentTooManyColumnsException</span><span class="sxs-lookup"><span data-stu-id="dae6b-121">EsentTooManyColumnsException members</span></span>](./esenttoomanycolumnsexception-members.md)

[<span data-ttu-id="dae6b-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="dae6b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
