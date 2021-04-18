---
description: 'Altre informazioni su: classe EsentOutOfObjectIDsException'
title: Classe EsentOutOfObjectIDsException
TOCTitle: EsentOutOfObjectIDsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofobjectidsexception(v=EXCHG.10)
ms:contentKeyID: 55102436
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 18cf8d1b7c98db8f855cf970eed7be87185fc9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316530"
---
# <a name="esentoutofobjectidsexception-class"></a><span data-ttu-id="f2779-103">Classe EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="f2779-103">EsentOutOfObjectIDsException class</span></span>

<span data-ttu-id="f2779-104">Classe di base per JET_err. Eccezioni OutOfObjectIDs.</span><span class="sxs-lookup"><span data-stu-id="f2779-104">Base class for JET_err.OutOfObjectIDs exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="f2779-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="f2779-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="f2779-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="f2779-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="f2779-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="f2779-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="f2779-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="f2779-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="f2779-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="f2779-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="f2779-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="f2779-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="f2779-111">Microsoft. ISAM. esent. Interop. EsentFragmentationException</span><span class="sxs-lookup"><span data-stu-id="f2779-111">Microsoft.Isam.Esent.Interop.EsentFragmentationException</span></span>](./esentfragmentationexception-class.md)  
            <span data-ttu-id="f2779-112">Microsoft. ISAM. esent. Interop. EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="f2779-112">Microsoft.Isam.Esent.Interop.EsentOutOfObjectIDsException</span></span>  

<span data-ttu-id="f2779-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f2779-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f2779-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f2779-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f2779-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2779-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfObjectIDsException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentOutOfObjectIDsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfObjectIDsException : EsentFragmentationException
```

## <a name="thread-safety"></a><span data-ttu-id="f2779-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="f2779-116">Thread safety</span></span>

<span data-ttu-id="f2779-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="f2779-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="f2779-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="f2779-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2779-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2779-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f2779-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f2779-120">Reference</span></span>

[<span data-ttu-id="f2779-121">Membri di EsentOutOfObjectIDsException</span><span class="sxs-lookup"><span data-stu-id="f2779-121">EsentOutOfObjectIDsException members</span></span>](./esentoutofobjectidsexception-members.md)

[<span data-ttu-id="f2779-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f2779-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
