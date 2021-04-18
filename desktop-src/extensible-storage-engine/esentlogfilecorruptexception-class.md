---
description: 'Altre informazioni su: classe EsentLogFileCorruptException'
title: Classe EsentLogFileCorruptException
TOCTitle: EsentLogFileCorruptException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogfilecorruptexception(v=EXCHG.10)
ms:contentKeyID: 55102161
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f2a3fa54d83cd1e88597b3689619e48a2372952e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312626"
---
# <a name="esentlogfilecorruptexception-class"></a><span data-ttu-id="d05e8-103">Classe EsentLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="d05e8-103">EsentLogFileCorruptException class</span></span>

<span data-ttu-id="d05e8-104">Classe di base per JET_err. Eccezioni LogFileCorrupt.</span><span class="sxs-lookup"><span data-stu-id="d05e8-104">Base class for JET_err.LogFileCorrupt exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="d05e8-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="d05e8-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="d05e8-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="d05e8-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="d05e8-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="d05e8-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="d05e8-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="d05e8-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="d05e8-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="d05e8-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="d05e8-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="d05e8-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="d05e8-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="d05e8-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="d05e8-112">Microsoft. ISAM. esent. Interop. EsentLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="d05e8-112">Microsoft.Isam.Esent.Interop.EsentLogFileCorruptException</span></span>  

<span data-ttu-id="d05e8-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d05e8-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d05e8-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d05e8-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d05e8-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d05e8-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogFileCorruptException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogFileCorruptException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogFileCorruptException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="d05e8-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="d05e8-116">Thread safety</span></span>

<span data-ttu-id="d05e8-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="d05e8-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="d05e8-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="d05e8-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="d05e8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d05e8-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d05e8-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d05e8-120">Reference</span></span>

[<span data-ttu-id="d05e8-121">Membri di EsentLogFileCorruptException</span><span class="sxs-lookup"><span data-stu-id="d05e8-121">EsentLogFileCorruptException members</span></span>](./esentlogfilecorruptexception-members.md)

[<span data-ttu-id="d05e8-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d05e8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
