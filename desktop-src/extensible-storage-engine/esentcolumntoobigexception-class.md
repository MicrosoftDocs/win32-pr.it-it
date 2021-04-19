---
description: 'Altre informazioni su: classe EsentColumnTooBigException'
title: Classe EsentColumnTooBigException
TOCTitle: EsentColumnTooBigException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentColumnTooBigException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentcolumntoobigexception(v=EXCHG.10)
ms:contentKeyID: 55101348
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentColumnTooBigException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentColumnTooBigException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a72ef8849dcbb8854786d126899924f0d835dcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319785"
---
# <a name="esentcolumntoobigexception-class"></a><span data-ttu-id="ab8b8-103">Classe EsentColumnTooBigException</span><span class="sxs-lookup"><span data-stu-id="ab8b8-103">EsentColumnTooBigException class</span></span>

<span data-ttu-id="ab8b8-104">Classe di base per JET_err. Eccezioni ColumnTooBig.</span><span class="sxs-lookup"><span data-stu-id="ab8b8-104">Base class for JET_err.ColumnTooBig exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="ab8b8-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="ab8b8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="ab8b8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="ab8b8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="ab8b8-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="ab8b8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="ab8b8-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="ab8b8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="ab8b8-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="ab8b8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="ab8b8-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="ab8b8-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="ab8b8-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="ab8b8-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="ab8b8-112">Microsoft. ISAM. esent. Interop. EsentColumnTooBigException</span><span class="sxs-lookup"><span data-stu-id="ab8b8-112">Microsoft.Isam.Esent.Interop.EsentColumnTooBigException</span></span>  

<span data-ttu-id="ab8b8-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ab8b8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ab8b8-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ab8b8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ab8b8-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab8b8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentColumnTooBigException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentColumnTooBigException
```

``` csharp
[SerializableAttribute]
public sealed class EsentColumnTooBigException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="ab8b8-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="ab8b8-116">Thread safety</span></span>

<span data-ttu-id="ab8b8-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="ab8b8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="ab8b8-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="ab8b8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab8b8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab8b8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ab8b8-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ab8b8-120">Reference</span></span>

[<span data-ttu-id="ab8b8-121">Membri di EsentColumnTooBigException</span><span class="sxs-lookup"><span data-stu-id="ab8b8-121">EsentColumnTooBigException members</span></span>](./esentcolumntoobigexception-members.md)

[<span data-ttu-id="ab8b8-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ab8b8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
