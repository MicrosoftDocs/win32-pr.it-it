---
description: 'Altre informazioni su: classe EsentSessionContextAlreadySetException'
title: Classe EsentSessionContextAlreadySetException
TOCTitle: EsentSessionContextAlreadySetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionContextAlreadySetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessioncontextalreadysetexception(v=EXCHG.10)
ms:contentKeyID: 55102703
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionContextAlreadySetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionContextAlreadySetException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a1365fd7f37b83e1be8007aa91db1b5f21bb383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313625"
---
# <a name="esentsessioncontextalreadysetexception-class"></a><span data-ttu-id="8866c-103">Classe EsentSessionContextAlreadySetException</span><span class="sxs-lookup"><span data-stu-id="8866c-103">EsentSessionContextAlreadySetException class</span></span>

<span data-ttu-id="8866c-104">Classe di base per JET_err. Eccezioni SessionContextAlreadySet.</span><span class="sxs-lookup"><span data-stu-id="8866c-104">Base class for JET_err.SessionContextAlreadySet exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8866c-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="8866c-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8866c-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8866c-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8866c-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="8866c-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8866c-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8866c-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8866c-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8866c-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8866c-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="8866c-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="8866c-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="8866c-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="8866c-112">Microsoft. ISAM. esent. Interop. EsentSessionContextAlreadySetException</span><span class="sxs-lookup"><span data-stu-id="8866c-112">Microsoft.Isam.Esent.Interop.EsentSessionContextAlreadySetException</span></span>  

<span data-ttu-id="8866c-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8866c-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8866c-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8866c-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8866c-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8866c-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionContextAlreadySetException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionContextAlreadySetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionContextAlreadySetException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="8866c-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="8866c-116">Thread safety</span></span>

<span data-ttu-id="8866c-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8866c-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8866c-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8866c-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8866c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8866c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8866c-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8866c-120">Reference</span></span>

[<span data-ttu-id="8866c-121">Membri di EsentSessionContextAlreadySetException</span><span class="sxs-lookup"><span data-stu-id="8866c-121">EsentSessionContextAlreadySetException members</span></span>](./esentsessioncontextalreadysetexception-members.md)

[<span data-ttu-id="8866c-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8866c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
