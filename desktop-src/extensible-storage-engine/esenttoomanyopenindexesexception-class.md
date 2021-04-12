---
description: 'Altre informazioni su: classe EsentTooManyOpenIndexesException'
title: Classe EsentTooManyOpenIndexesException
TOCTitle: EsentTooManyOpenIndexesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopenindexesexception(v=EXCHG.10)
ms:contentKeyID: 55103106
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 681f9a8ec67b9b9c82babcc3814833a1a3dbb0d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233383"
---
# <a name="esenttoomanyopenindexesexception-class"></a><span data-ttu-id="c83b1-103">Classe EsentTooManyOpenIndexesException</span><span class="sxs-lookup"><span data-stu-id="c83b1-103">EsentTooManyOpenIndexesException class</span></span>

<span data-ttu-id="c83b1-104">Classe di base per JET_err. Eccezioni TooManyOpenIndexes.</span><span class="sxs-lookup"><span data-stu-id="c83b1-104">Base class for JET_err.TooManyOpenIndexes exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c83b1-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="c83b1-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c83b1-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c83b1-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c83b1-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c83b1-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c83b1-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c83b1-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c83b1-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c83b1-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c83b1-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="c83b1-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="c83b1-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="c83b1-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="c83b1-112">Microsoft. ISAM. esent. Interop. EsentMemoryException</span><span class="sxs-lookup"><span data-stu-id="c83b1-112">Microsoft.Isam.Esent.Interop.EsentMemoryException</span></span>](./esentmemoryexception-class.md)  
              <span data-ttu-id="c83b1-113">Microsoft. ISAM. esent. Interop. EsentTooManyOpenIndexesException</span><span class="sxs-lookup"><span data-stu-id="c83b1-113">Microsoft.Isam.Esent.Interop.EsentTooManyOpenIndexesException</span></span>  

<span data-ttu-id="c83b1-114">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c83b1-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c83b1-115">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c83b1-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c83b1-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c83b1-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenIndexesException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentTooManyOpenIndexesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenIndexesException : EsentMemoryException
```

## <a name="thread-safety"></a><span data-ttu-id="c83b1-117">Thread safety</span><span class="sxs-lookup"><span data-stu-id="c83b1-117">Thread safety</span></span>

<span data-ttu-id="c83b1-118">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c83b1-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c83b1-119">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c83b1-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c83b1-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c83b1-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c83b1-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c83b1-121">Reference</span></span>

[<span data-ttu-id="c83b1-122">Membri di EsentTooManyOpenIndexesException</span><span class="sxs-lookup"><span data-stu-id="c83b1-122">EsentTooManyOpenIndexesException members</span></span>](./esenttoomanyopenindexesexception-members.md)

[<span data-ttu-id="c83b1-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c83b1-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
