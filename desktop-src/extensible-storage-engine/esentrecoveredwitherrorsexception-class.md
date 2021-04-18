---
description: 'Altre informazioni su: classe EsentRecoveredWithErrorsException'
title: Classe EsentRecoveredWithErrorsException
TOCTitle: EsentRecoveredWithErrorsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrecoveredwitherrorsexception(v=EXCHG.10)
ms:contentKeyID: 55102545
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd90328b3b592232e1f87f4fe568022443be8b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308044"
---
# <a name="esentrecoveredwitherrorsexception-class"></a><span data-ttu-id="59540-103">Classe EsentRecoveredWithErrorsException</span><span class="sxs-lookup"><span data-stu-id="59540-103">EsentRecoveredWithErrorsException class</span></span>

<span data-ttu-id="59540-104">Classe di base per JET_err. Eccezioni RecoveredWithErrors.</span><span class="sxs-lookup"><span data-stu-id="59540-104">Base class for JET_err.RecoveredWithErrors exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="59540-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="59540-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="59540-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="59540-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="59540-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="59540-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="59540-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="59540-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="59540-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="59540-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="59540-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="59540-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="59540-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="59540-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="59540-112">Microsoft. ISAM. esent. Interop. EsentRecoveredWithErrorsException</span><span class="sxs-lookup"><span data-stu-id="59540-112">Microsoft.Isam.Esent.Interop.EsentRecoveredWithErrorsException</span></span>  

<span data-ttu-id="59540-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="59540-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="59540-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="59540-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="59540-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="59540-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRecoveredWithErrorsException _
    Inherits EsentStateException
'Usage
Dim instance As EsentRecoveredWithErrorsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRecoveredWithErrorsException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="59540-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="59540-116">Thread safety</span></span>

<span data-ttu-id="59540-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="59540-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="59540-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="59540-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="59540-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="59540-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="59540-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="59540-120">Reference</span></span>

[<span data-ttu-id="59540-121">Membri di EsentRecoveredWithErrorsException</span><span class="sxs-lookup"><span data-stu-id="59540-121">EsentRecoveredWithErrorsException members</span></span>](./esentrecoveredwitherrorsexception-members.md)

[<span data-ttu-id="59540-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="59540-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
