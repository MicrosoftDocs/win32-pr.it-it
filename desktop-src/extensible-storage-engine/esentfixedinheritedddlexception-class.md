---
description: 'Altre informazioni su: classe EsentFixedInheritedDDLException'
title: Classe EsentFixedInheritedDDLException
TOCTitle: EsentFixedInheritedDDLException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfixedinheritedddlexception(v=EXCHG.10)
ms:contentKeyID: 55101724
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43f8638b396848503819635860b7472a8af684c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309695"
---
# <a name="esentfixedinheritedddlexception-class"></a><span data-ttu-id="be2cb-103">Classe EsentFixedInheritedDDLException</span><span class="sxs-lookup"><span data-stu-id="be2cb-103">EsentFixedInheritedDDLException class</span></span>

<span data-ttu-id="be2cb-104">Classe di base per JET_err. Eccezioni FixedInheritedDDL.</span><span class="sxs-lookup"><span data-stu-id="be2cb-104">Base class for JET_err.FixedInheritedDDL exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="be2cb-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="be2cb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="be2cb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="be2cb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="be2cb-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="be2cb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="be2cb-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="be2cb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="be2cb-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="be2cb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="be2cb-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="be2cb-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="be2cb-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="be2cb-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="be2cb-112">Microsoft. ISAM. esent. Interop. EsentFixedInheritedDDLException</span><span class="sxs-lookup"><span data-stu-id="be2cb-112">Microsoft.Isam.Esent.Interop.EsentFixedInheritedDDLException</span></span>  

<span data-ttu-id="be2cb-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="be2cb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="be2cb-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="be2cb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="be2cb-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be2cb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFixedInheritedDDLException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentFixedInheritedDDLException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFixedInheritedDDLException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="be2cb-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="be2cb-116">Thread safety</span></span>

<span data-ttu-id="be2cb-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="be2cb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="be2cb-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="be2cb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="be2cb-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be2cb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="be2cb-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="be2cb-120">Reference</span></span>

[<span data-ttu-id="be2cb-121">Membri di EsentFixedInheritedDDLException</span><span class="sxs-lookup"><span data-stu-id="be2cb-121">EsentFixedInheritedDDLException members</span></span>](./esentfixedinheritedddlexception-members.md)

[<span data-ttu-id="be2cb-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="be2cb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
