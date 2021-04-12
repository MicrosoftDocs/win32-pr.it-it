---
description: 'Altre informazioni su: classe EsentDiskReadVerificationFailureException'
title: Classe EsentDiskReadVerificationFailureException
TOCTitle: EsentDiskReadVerificationFailureException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdiskreadverificationfailureexception(v=EXCHG.10)
ms:contentKeyID: 55101620
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f429efb66f5993f438e132ed564f110e88d234a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233766"
---
# <a name="esentdiskreadverificationfailureexception-class"></a><span data-ttu-id="2e5ed-103">Classe EsentDiskReadVerificationFailureException</span><span class="sxs-lookup"><span data-stu-id="2e5ed-103">EsentDiskReadVerificationFailureException class</span></span>

<span data-ttu-id="2e5ed-104">Classe di base per JET_err. Eccezioni DiskReadVerificationFailure.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-104">Base class for JET_err.DiskReadVerificationFailure exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2e5ed-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="2e5ed-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2e5ed-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2e5ed-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2e5ed-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2e5ed-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2e5ed-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2e5ed-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2e5ed-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2e5ed-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2e5ed-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="2e5ed-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="2e5ed-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2e5ed-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="2e5ed-112">Microsoft. ISAM. esent. Interop. EsentDiskReadVerificationFailureException</span><span class="sxs-lookup"><span data-stu-id="2e5ed-112">Microsoft.Isam.Esent.Interop.EsentDiskReadVerificationFailureException</span></span>  

<span data-ttu-id="2e5ed-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2e5ed-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2e5ed-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2e5ed-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2e5ed-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2e5ed-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDiskReadVerificationFailureException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDiskReadVerificationFailureException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDiskReadVerificationFailureException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="2e5ed-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="2e5ed-116">Thread safety</span></span>

<span data-ttu-id="2e5ed-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2e5ed-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="2e5ed-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e5ed-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e5ed-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2e5ed-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2e5ed-120">Reference</span></span>

[<span data-ttu-id="2e5ed-121">Membri di EsentDiskReadVerificationFailureException</span><span class="sxs-lookup"><span data-stu-id="2e5ed-121">EsentDiskReadVerificationFailureException members</span></span>](./esentdiskreadverificationfailureexception-members.md)

[<span data-ttu-id="2e5ed-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2e5ed-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
