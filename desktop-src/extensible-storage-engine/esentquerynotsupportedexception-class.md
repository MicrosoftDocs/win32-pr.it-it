---
description: 'Altre informazioni su: classe EsentQueryNotSupportedException'
title: Classe EsentQueryNotSupportedException
TOCTitle: EsentQueryNotSupportedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquerynotsupportedexception(v=EXCHG.10)
ms:contentKeyID: 55107329
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f67b181d509335a94ebd5cdb1c6f4a18e57a4886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401721"
---
# <a name="esentquerynotsupportedexception-class"></a><span data-ttu-id="53c20-103">Classe EsentQueryNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="53c20-103">EsentQueryNotSupportedException class</span></span>

<span data-ttu-id="53c20-104">Classe di base per JET_err. Eccezioni QueryNotSupported.</span><span class="sxs-lookup"><span data-stu-id="53c20-104">Base class for JET_err.QueryNotSupported exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="53c20-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="53c20-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="53c20-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="53c20-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="53c20-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="53c20-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="53c20-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="53c20-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="53c20-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="53c20-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="53c20-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="53c20-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="53c20-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="53c20-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="53c20-112">Microsoft. ISAM. esent. Interop. EsentQueryNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="53c20-112">Microsoft.Isam.Esent.Interop.EsentQueryNotSupportedException</span></span>  

<span data-ttu-id="53c20-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53c20-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53c20-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53c20-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53c20-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53c20-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentQueryNotSupportedException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentQueryNotSupportedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentQueryNotSupportedException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="53c20-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="53c20-116">Thread safety</span></span>

<span data-ttu-id="53c20-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="53c20-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="53c20-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="53c20-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="53c20-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53c20-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53c20-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="53c20-120">Reference</span></span>

[<span data-ttu-id="53c20-121">Membri di EsentQueryNotSupportedException</span><span class="sxs-lookup"><span data-stu-id="53c20-121">EsentQueryNotSupportedException members</span></span>](./esentquerynotsupportedexception-members.md)

[<span data-ttu-id="53c20-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="53c20-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
