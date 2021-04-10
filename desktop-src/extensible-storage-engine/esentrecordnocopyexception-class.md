---
description: 'Altre informazioni su: classe EsentRecordNoCopyException'
title: Classe EsentRecordNoCopyException
TOCTitle: EsentRecordNoCopyException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordnocopyexception(v=EXCHG.10)
ms:contentKeyID: 55102583
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cca22790cc7cc45199be939a9acad944ab2f613e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231988"
---
# <a name="esentrecordnocopyexception-class"></a><span data-ttu-id="b6347-103">Classe EsentRecordNoCopyException</span><span class="sxs-lookup"><span data-stu-id="b6347-103">EsentRecordNoCopyException class</span></span>

<span data-ttu-id="b6347-104">Classe di base per JET_err. Eccezioni RecordNoCopy.</span><span class="sxs-lookup"><span data-stu-id="b6347-104">Base class for JET_err.RecordNoCopy exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b6347-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="b6347-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b6347-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b6347-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b6347-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b6347-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b6347-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b6347-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b6347-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b6347-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b6347-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b6347-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b6347-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="b6347-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="b6347-112">Microsoft. ISAM. esent. Interop. EsentRecordNoCopyException</span><span class="sxs-lookup"><span data-stu-id="b6347-112">Microsoft.Isam.Esent.Interop.EsentRecordNoCopyException</span></span>  

<span data-ttu-id="b6347-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b6347-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b6347-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b6347-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b6347-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6347-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordNoCopyException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentRecordNoCopyException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordNoCopyException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="b6347-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="b6347-116">Thread safety</span></span>

<span data-ttu-id="b6347-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b6347-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b6347-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b6347-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6347-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6347-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6347-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b6347-120">Reference</span></span>

[<span data-ttu-id="b6347-121">Membri di EsentRecordNoCopyException</span><span class="sxs-lookup"><span data-stu-id="b6347-121">EsentRecordNoCopyException members</span></span>](./esentrecordnocopyexception-members.md)

[<span data-ttu-id="b6347-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b6347-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
