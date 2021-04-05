---
description: 'Altre informazioni su: classe EsentRecordTooBigForBackwardCompatibilityException'
title: Classe EsentRecordTooBigForBackwardCompatibilityException
TOCTitle: EsentRecordTooBigForBackwardCompatibilityException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecordtoobigforbackwardcompatibilityexception(v=EXCHG.10)
ms:contentKeyID: 55102602
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b3d56e87678daf465f3f303d649e8c554fbb0c21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750698"
---
# <a name="esentrecordtoobigforbackwardcompatibilityexception-class"></a><span data-ttu-id="f34fe-103">Classe EsentRecordTooBigForBackwardCompatibilityException</span><span class="sxs-lookup"><span data-stu-id="f34fe-103">EsentRecordTooBigForBackwardCompatibilityException class</span></span>

<span data-ttu-id="f34fe-104">Classe di base per JET_err. Eccezioni RecordTooBigForBackwardCompatibility.</span><span class="sxs-lookup"><span data-stu-id="f34fe-104">Base class for JET_err.RecordTooBigForBackwardCompatibility exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f34fe-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="f34fe-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f34fe-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f34fe-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f34fe-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f34fe-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f34fe-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f34fe-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f34fe-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f34fe-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f34fe-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="f34fe-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="f34fe-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="f34fe-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="f34fe-112">Microsoft. ISAM. esent. Interop. EsentRecordTooBigForBackwardCompatibilityException</span><span class="sxs-lookup"><span data-stu-id="f34fe-112">Microsoft.Isam.Esent.Interop.EsentRecordTooBigForBackwardCompatibilityException</span></span>  

<span data-ttu-id="f34fe-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f34fe-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f34fe-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f34fe-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f34fe-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f34fe-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecordTooBigForBackwardCompatibilityException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecordTooBigForBackwardCompatibilityException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecordTooBigForBackwardCompatibilityException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="f34fe-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="f34fe-116">Thread safety</span></span>

<span data-ttu-id="f34fe-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f34fe-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f34fe-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f34fe-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f34fe-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f34fe-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f34fe-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f34fe-120">Reference</span></span>

[<span data-ttu-id="f34fe-121">Membri di EsentRecordTooBigForBackwardCompatibilityException</span><span class="sxs-lookup"><span data-stu-id="f34fe-121">EsentRecordTooBigForBackwardCompatibilityException members</span></span>](./esentrecordtoobigforbackwardcompatibilityexception-members.md)

[<span data-ttu-id="f34fe-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f34fe-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
