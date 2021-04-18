---
description: 'Altre informazioni su: classe EsentColumnRedundantException'
title: Classe EsentColumnRedundantException
TOCTitle: EsentColumnRedundantException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnRedundantException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumnredundantexception(v=EXCHG.10)
ms:contentKeyID: 55101247
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnRedundantException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnRedundantException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18b2fdd850e26c5a435841110a4e1ac5c0c7c640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305820"
---
# <a name="esentcolumnredundantexception-class"></a><span data-ttu-id="2d625-103">Classe EsentColumnRedundantException</span><span class="sxs-lookup"><span data-stu-id="2d625-103">EsentColumnRedundantException class</span></span>

<span data-ttu-id="2d625-104">Classe di base per JET_err. Eccezioni ColumnRedundant.</span><span class="sxs-lookup"><span data-stu-id="2d625-104">Base class for JET_err.ColumnRedundant exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2d625-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="2d625-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2d625-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2d625-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2d625-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2d625-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2d625-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2d625-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2d625-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2d625-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2d625-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="2d625-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="2d625-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="2d625-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="2d625-112">Microsoft. ISAM. esent. Interop. EsentColumnRedundantException</span><span class="sxs-lookup"><span data-stu-id="2d625-112">Microsoft.Isam.Esent.Interop.EsentColumnRedundantException</span></span>  

<span data-ttu-id="2d625-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2d625-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2d625-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2d625-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2d625-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d625-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnRedundantException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnRedundantException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnRedundantException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="2d625-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="2d625-116">Thread safety</span></span>

<span data-ttu-id="2d625-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2d625-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2d625-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="2d625-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2d625-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d625-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2d625-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2d625-120">Reference</span></span>

[<span data-ttu-id="2d625-121">Membri di EsentColumnRedundantException</span><span class="sxs-lookup"><span data-stu-id="2d625-121">EsentColumnRedundantException members</span></span>](./esentcolumnredundantexception-members.md)

[<span data-ttu-id="2d625-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2d625-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
