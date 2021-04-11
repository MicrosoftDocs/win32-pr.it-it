---
description: 'Altre informazioni su: classe EsentDatabaseFailedIncrementalReseedException'
title: Classe EsentDatabaseFailedIncrementalReseedException
TOCTitle: EsentDatabaseFailedIncrementalReseedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasefailedincrementalreseedexception(v=EXCHG.10)
ms:contentKeyID: 55101465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cfa0f4a82e3a8936ee3e7a262f8079396b95a54a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129595"
---
# <a name="esentdatabasefailedincrementalreseedexception-class"></a><span data-ttu-id="601bd-103">Classe EsentDatabaseFailedIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="601bd-103">EsentDatabaseFailedIncrementalReseedException class</span></span>

<span data-ttu-id="601bd-104">Classe di base per JET_err. Eccezioni DatabaseFailedIncrementalReseed.</span><span class="sxs-lookup"><span data-stu-id="601bd-104">Base class for JET_err.DatabaseFailedIncrementalReseed exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="601bd-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="601bd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="601bd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="601bd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="601bd-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="601bd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="601bd-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="601bd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="601bd-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="601bd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="601bd-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="601bd-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="601bd-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="601bd-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="601bd-112">Microsoft. ISAM. esent. Interop. EsentDatabaseFailedIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="601bd-112">Microsoft.Isam.Esent.Interop.EsentDatabaseFailedIncrementalReseedException</span></span>  

<span data-ttu-id="601bd-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="601bd-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="601bd-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="601bd-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="601bd-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="601bd-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseFailedIncrementalReseedException _
    Inherits EsentStateException
'Usage
Dim instance As EsentDatabaseFailedIncrementalReseedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseFailedIncrementalReseedException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="601bd-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="601bd-116">Thread safety</span></span>

<span data-ttu-id="601bd-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="601bd-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="601bd-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="601bd-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="601bd-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="601bd-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="601bd-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="601bd-120">Reference</span></span>

[<span data-ttu-id="601bd-121">Membri di EsentDatabaseFailedIncrementalReseedException</span><span class="sxs-lookup"><span data-stu-id="601bd-121">EsentDatabaseFailedIncrementalReseedException members</span></span>](./esentdatabasefailedincrementalreseedexception-members.md)

[<span data-ttu-id="601bd-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="601bd-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
