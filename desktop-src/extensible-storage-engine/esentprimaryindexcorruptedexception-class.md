---
description: 'Altre informazioni su: classe EsentPrimaryIndexCorruptedException'
title: Classe EsentPrimaryIndexCorruptedException
TOCTitle: EsentPrimaryIndexCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentprimaryindexcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55102484
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6a2d95d50e7cb8ba7bb962686e3c452c35c3b295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317451"
---
# <a name="esentprimaryindexcorruptedexception-class"></a><span data-ttu-id="c6481-103">Classe EsentPrimaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="c6481-103">EsentPrimaryIndexCorruptedException class</span></span>

<span data-ttu-id="c6481-104">Classe di base per JET_err. Eccezioni PrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="c6481-104">Base class for JET_err.PrimaryIndexCorrupted exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="c6481-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="c6481-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="c6481-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="c6481-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="c6481-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="c6481-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="c6481-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="c6481-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="c6481-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="c6481-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="c6481-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="c6481-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="c6481-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="c6481-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="c6481-112">Microsoft. ISAM. esent. Interop. EsentPrimaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="c6481-112">Microsoft.Isam.Esent.Interop.EsentPrimaryIndexCorruptedException</span></span>  

<span data-ttu-id="c6481-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c6481-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c6481-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c6481-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c6481-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6481-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPrimaryIndexCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentPrimaryIndexCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPrimaryIndexCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="c6481-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="c6481-116">Thread safety</span></span>

<span data-ttu-id="c6481-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="c6481-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="c6481-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="c6481-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="c6481-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6481-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c6481-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c6481-120">Reference</span></span>

[<span data-ttu-id="c6481-121">Membri di EsentPrimaryIndexCorruptedException</span><span class="sxs-lookup"><span data-stu-id="c6481-121">EsentPrimaryIndexCorruptedException members</span></span>](./esentprimaryindexcorruptedexception-members.md)

[<span data-ttu-id="c6481-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c6481-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
