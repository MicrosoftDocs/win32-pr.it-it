---
description: 'Altre informazioni su: classe EsentNoCurrentRecordException'
title: Classe EsentNoCurrentRecordException
TOCTitle: EsentNoCurrentRecordException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnocurrentrecordexception(v=EXCHG.10)
ms:contentKeyID: 55102290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed58890ccd410101ecc6e6f38fafa0d254f4c2d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319239"
---
# <a name="esentnocurrentrecordexception-class"></a><span data-ttu-id="b8e2e-103">Classe EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="b8e2e-103">EsentNoCurrentRecordException class</span></span>

<span data-ttu-id="b8e2e-104">Classe di base per JET_err. Eccezioni NoCurrentRecord.</span><span class="sxs-lookup"><span data-stu-id="b8e2e-104">Base class for JET_err.NoCurrentRecord exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b8e2e-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="b8e2e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b8e2e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b8e2e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b8e2e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="b8e2e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b8e2e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="b8e2e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b8e2e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="b8e2e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="b8e2e-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="b8e2e-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="b8e2e-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="b8e2e-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="b8e2e-112">Microsoft. ISAM. esent. Interop. EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="b8e2e-112">Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException</span></span>  

<span data-ttu-id="b8e2e-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b8e2e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b8e2e-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b8e2e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e2e-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8e2e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoCurrentRecordException _
    Inherits EsentStateException
'Usage
Dim instance As EsentNoCurrentRecordException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoCurrentRecordException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="b8e2e-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="b8e2e-116">Thread safety</span></span>

<span data-ttu-id="b8e2e-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="b8e2e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b8e2e-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b8e2e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b8e2e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8e2e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b8e2e-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b8e2e-120">Reference</span></span>

[<span data-ttu-id="b8e2e-121">Membri di EsentNoCurrentRecordException</span><span class="sxs-lookup"><span data-stu-id="b8e2e-121">EsentNoCurrentRecordException members</span></span>](./esentnocurrentrecordexception-members.md)

[<span data-ttu-id="b8e2e-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b8e2e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
