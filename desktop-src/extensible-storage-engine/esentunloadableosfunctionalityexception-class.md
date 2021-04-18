---
description: 'Altre informazioni su: classe EsentUnloadableOSFunctionalityException'
title: Classe EsentUnloadableOSFunctionalityException
TOCTitle: EsentUnloadableOSFunctionalityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentunloadableosfunctionalityexception(v=EXCHG.10)
ms:contentKeyID: 55107333
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 81b1151be5020a07f92582e762c6e6597138d9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315178"
---
# <a name="esentunloadableosfunctionalityexception-class"></a><span data-ttu-id="c7fc4-103">Classe EsentUnloadableOSFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="c7fc4-103">EsentUnloadableOSFunctionalityException class</span></span>

<span data-ttu-id="c7fc4-104">Classe di base per JET_err. Eccezioni UnloadableOSFunctionality.</span><span class="sxs-lookup"><span data-stu-id="c7fc4-104">Base class for JET_err.UnloadableOSFunctionality exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c7fc4-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="c7fc4-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c7fc4-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c7fc4-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c7fc4-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c7fc4-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c7fc4-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c7fc4-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c7fc4-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c7fc4-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c7fc4-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c7fc4-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c7fc4-111">Microsoft. ISAM. esent. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="c7fc4-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="c7fc4-112">Microsoft. ISAM. esent. Interop. EsentUnloadableOSFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="c7fc4-112">Microsoft.Isam.Esent.Interop.EsentUnloadableOSFunctionalityException</span></span>  

<span data-ttu-id="c7fc4-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c7fc4-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c7fc4-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c7fc4-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fc4-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7fc4-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentUnloadableOSFunctionalityException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentUnloadableOSFunctionalityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentUnloadableOSFunctionalityException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="c7fc4-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="c7fc4-116">Thread safety</span></span>

<span data-ttu-id="c7fc4-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c7fc4-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c7fc4-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c7fc4-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7fc4-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7fc4-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c7fc4-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c7fc4-120">Reference</span></span>

[<span data-ttu-id="c7fc4-121">Membri di EsentUnloadableOSFunctionalityException</span><span class="sxs-lookup"><span data-stu-id="c7fc4-121">EsentUnloadableOSFunctionalityException members</span></span>](./esentunloadableosfunctionalityexception-members.md)

[<span data-ttu-id="c7fc4-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c7fc4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
