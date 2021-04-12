---
description: 'Altre informazioni su: classe EsentBadEmptyPageException'
title: Classe EsentBadEmptyPageException
TOCTitle: EsentBadEmptyPageException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbademptypageexception(v=EXCHG.10)
ms:contentKeyID: 55101115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 144f42c42eaf3ccb804344214d396cd8ac2f8aa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232779"
---
# <a name="esentbademptypageexception-class"></a><span data-ttu-id="2b14a-103">Classe EsentBadEmptyPageException</span><span class="sxs-lookup"><span data-stu-id="2b14a-103">EsentBadEmptyPageException class</span></span>

<span data-ttu-id="2b14a-104">Classe di base per JET_err. Eccezioni BadEmptyPage.</span><span class="sxs-lookup"><span data-stu-id="2b14a-104">Base class for JET_err.BadEmptyPage exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="2b14a-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="2b14a-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="2b14a-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="2b14a-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="2b14a-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="2b14a-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="2b14a-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="2b14a-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="2b14a-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="2b14a-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="2b14a-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="2b14a-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="2b14a-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="2b14a-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="2b14a-112">Microsoft. ISAM. esent. Interop. EsentBadEmptyPageException</span><span class="sxs-lookup"><span data-stu-id="2b14a-112">Microsoft.Isam.Esent.Interop.EsentBadEmptyPageException</span></span>  

<span data-ttu-id="2b14a-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2b14a-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2b14a-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2b14a-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2b14a-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b14a-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBadEmptyPageException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentBadEmptyPageException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBadEmptyPageException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="2b14a-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="2b14a-116">Thread safety</span></span>

<span data-ttu-id="2b14a-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2b14a-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="2b14a-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="2b14a-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b14a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b14a-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2b14a-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2b14a-120">Reference</span></span>

[<span data-ttu-id="2b14a-121">Membri di EsentBadEmptyPageException</span><span class="sxs-lookup"><span data-stu-id="2b14a-121">EsentBadEmptyPageException members</span></span>](./esentbademptypageexception-members.md)

[<span data-ttu-id="2b14a-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2b14a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
