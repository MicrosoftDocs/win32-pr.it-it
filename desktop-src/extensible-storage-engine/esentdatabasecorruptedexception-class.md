---
description: 'Altre informazioni su: classe EsentDatabaseCorruptedException'
title: Classe EsentDatabaseCorruptedException
TOCTitle: EsentDatabaseCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabasecorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55101330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a82a0ec101223bae64b39a4db2ca0779d671591c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879718"
---
# <a name="esentdatabasecorruptedexception-class"></a><span data-ttu-id="e7484-103">Classe EsentDatabaseCorruptedException</span><span class="sxs-lookup"><span data-stu-id="e7484-103">EsentDatabaseCorruptedException class</span></span>

<span data-ttu-id="e7484-104">Classe di base per JET_err. Eccezioni DatabaseCorrupted.</span><span class="sxs-lookup"><span data-stu-id="e7484-104">Base class for JET_err.DatabaseCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e7484-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="e7484-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e7484-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e7484-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e7484-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e7484-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e7484-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="e7484-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e7484-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e7484-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e7484-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="e7484-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="e7484-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="e7484-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="e7484-112">Microsoft. ISAM. esent. Interop. EsentDatabaseCorruptedException</span><span class="sxs-lookup"><span data-stu-id="e7484-112">Microsoft.Isam.Esent.Interop.EsentDatabaseCorruptedException</span></span>  

<span data-ttu-id="e7484-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e7484-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e7484-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e7484-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e7484-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7484-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDatabaseCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="e7484-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="e7484-116">Thread safety</span></span>

<span data-ttu-id="e7484-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e7484-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e7484-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e7484-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7484-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7484-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e7484-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e7484-120">Reference</span></span>

[<span data-ttu-id="e7484-121">Membri di EsentDatabaseCorruptedException</span><span class="sxs-lookup"><span data-stu-id="e7484-121">EsentDatabaseCorruptedException members</span></span>](./esentdatabasecorruptedexception-members.md)

[<span data-ttu-id="e7484-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e7484-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
