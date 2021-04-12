---
description: 'Altre informazioni su: classe EsentLogSequenceEndException'
title: Classe EsentLogSequenceEndException
TOCTitle: EsentLogSequenceEndException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogsequenceendexception(v=EXCHG.10)
ms:contentKeyID: 55102213
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78de803d31d8e97f9493d605d688916501edba6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226749"
---
# <a name="esentlogsequenceendexception-class"></a><span data-ttu-id="a306f-103">Classe EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="a306f-103">EsentLogSequenceEndException class</span></span>

<span data-ttu-id="a306f-104">Classe di base per JET_err. Eccezioni LogSequenceEnd.</span><span class="sxs-lookup"><span data-stu-id="a306f-104">Base class for JET_err.LogSequenceEnd exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a306f-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="a306f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a306f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a306f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a306f-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a306f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a306f-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a306f-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a306f-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a306f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a306f-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="a306f-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="a306f-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="a306f-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="a306f-112">Microsoft. ISAM. esent. Interop. EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="a306f-112">Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException</span></span>  

<span data-ttu-id="a306f-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a306f-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a306f-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a306f-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a306f-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a306f-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogSequenceEndException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentLogSequenceEndException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogSequenceEndException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="a306f-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="a306f-116">Thread safety</span></span>

<span data-ttu-id="a306f-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a306f-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a306f-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a306f-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a306f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a306f-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a306f-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a306f-120">Reference</span></span>

[<span data-ttu-id="a306f-121">Membri di EsentLogSequenceEndException</span><span class="sxs-lookup"><span data-stu-id="a306f-121">EsentLogSequenceEndException members</span></span>](./esentlogsequenceendexception-members.md)

[<span data-ttu-id="a306f-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a306f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
