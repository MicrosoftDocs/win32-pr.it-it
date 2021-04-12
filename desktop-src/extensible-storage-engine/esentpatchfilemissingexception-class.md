---
description: 'Altre informazioni su: classe EsentPatchFileMissingException'
title: Classe EsentPatchFileMissingException
TOCTitle: EsentPatchFileMissingException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpatchfilemissingexception(v=EXCHG.10)
ms:contentKeyID: 55102469
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edaabc35018c7905542f9a7325efaed300234e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347591"
---
# <a name="esentpatchfilemissingexception-class"></a><span data-ttu-id="e4bbb-103">Classe EsentPatchFileMissingException</span><span class="sxs-lookup"><span data-stu-id="e4bbb-103">EsentPatchFileMissingException class</span></span>

<span data-ttu-id="e4bbb-104">Classe di base per JET_err. Eccezioni PatchFileMissing.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-104">Base class for JET_err.PatchFileMissing exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e4bbb-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="e4bbb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e4bbb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e4bbb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e4bbb-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e4bbb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e4bbb-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="e4bbb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e4bbb-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e4bbb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e4bbb-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="e4bbb-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="e4bbb-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="e4bbb-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="e4bbb-112">Microsoft. ISAM. esent. Interop. EsentPatchFileMissingException</span><span class="sxs-lookup"><span data-stu-id="e4bbb-112">Microsoft.Isam.Esent.Interop.EsentPatchFileMissingException</span></span>  

<span data-ttu-id="e4bbb-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4bbb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e4bbb-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e4bbb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4bbb-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4bbb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPatchFileMissingException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentPatchFileMissingException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPatchFileMissingException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="e4bbb-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="e4bbb-116">Thread safety</span></span>

<span data-ttu-id="e4bbb-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e4bbb-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e4bbb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4bbb-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4bbb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4bbb-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e4bbb-120">Reference</span></span>

[<span data-ttu-id="e4bbb-121">Membri di EsentPatchFileMissingException</span><span class="sxs-lookup"><span data-stu-id="e4bbb-121">EsentPatchFileMissingException members</span></span>](./esentpatchfilemissingexception-members.md)

[<span data-ttu-id="e4bbb-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e4bbb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
