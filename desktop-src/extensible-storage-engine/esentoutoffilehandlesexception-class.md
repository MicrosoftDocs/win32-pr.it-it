---
description: 'Altre informazioni su: classe EsentOutOfFileHandlesException'
title: Classe EsentOutOfFileHandlesException
TOCTitle: EsentOutOfFileHandlesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutoffilehandlesexception(v=EXCHG.10)
ms:contentKeyID: 55102419
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 24d8dec9de0cb4149835766222348dc037f54c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317458"
---
# <a name="esentoutoffilehandlesexception-class"></a><span data-ttu-id="34473-103">Classe EsentOutOfFileHandlesException</span><span class="sxs-lookup"><span data-stu-id="34473-103">EsentOutOfFileHandlesException class</span></span>

<span data-ttu-id="34473-104">Classe di base per JET_err. Eccezioni OutOfFileHandles.</span><span class="sxs-lookup"><span data-stu-id="34473-104">Base class for JET_err.OutOfFileHandles exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="34473-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="34473-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="34473-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="34473-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="34473-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="34473-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="34473-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="34473-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="34473-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="34473-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="34473-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="34473-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="34473-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="34473-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="34473-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="34473-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="34473-113">Microsoft. ISAM. esent. Interop. EsentOutOfFileHandlesException</span><span class="sxs-lookup"><span data-stu-id="34473-113">Microsoft.Isam.Esent.Interop.EsentOutOfFileHandlesException</span></span>  

<span data-ttu-id="34473-114">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34473-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34473-115">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34473-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34473-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34473-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfFileHandlesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfFileHandlesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfFileHandlesException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="34473-117">Thread safety</span><span class="sxs-lookup"><span data-stu-id="34473-117">Thread safety</span></span>

<span data-ttu-id="34473-118">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="34473-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="34473-119">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="34473-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="34473-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34473-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34473-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="34473-121">Reference</span></span>

[<span data-ttu-id="34473-122">Membri di EsentOutOfFileHandlesException</span><span class="sxs-lookup"><span data-stu-id="34473-122">EsentOutOfFileHandlesException members</span></span>](./esentoutoffilehandlesexception-members.md)

[<span data-ttu-id="34473-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="34473-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
