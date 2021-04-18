---
description: 'Altre informazioni su: classe EsentLogWriteFailException'
title: Classe EsentLogWriteFailException
TOCTitle: EsentLogWriteFailException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogwritefailexception(v=EXCHG.10)
ms:contentKeyID: 55102169
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogWriteFailException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9cd3fe6b541a58b7498ca4117f7ba2af7662d5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313635"
---
# <a name="esentlogwritefailexception-class"></a><span data-ttu-id="27fa2-103">Classe EsentLogWriteFailException</span><span class="sxs-lookup"><span data-stu-id="27fa2-103">EsentLogWriteFailException class</span></span>

<span data-ttu-id="27fa2-104">Classe di base per JET_err. Eccezioni LogWriteFail.</span><span class="sxs-lookup"><span data-stu-id="27fa2-104">Base class for JET_err.LogWriteFail exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="27fa2-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="27fa2-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="27fa2-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="27fa2-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="27fa2-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="27fa2-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="27fa2-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="27fa2-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="27fa2-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="27fa2-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="27fa2-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="27fa2-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="27fa2-111">Microsoft. ISAM. esent. Interop. EsentIOException</span><span class="sxs-lookup"><span data-stu-id="27fa2-111">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
            <span data-ttu-id="27fa2-112">Microsoft. ISAM. esent. Interop. EsentLogWriteFailException</span><span class="sxs-lookup"><span data-stu-id="27fa2-112">Microsoft.Isam.Esent.Interop.EsentLogWriteFailException</span></span>  

<span data-ttu-id="27fa2-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="27fa2-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="27fa2-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="27fa2-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="27fa2-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="27fa2-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogWriteFailException _
    Inherits EsentIOException
'Usage
Dim instance As EsentLogWriteFailException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogWriteFailException : EsentIOException
```

## <a name="thread-safety"></a><span data-ttu-id="27fa2-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="27fa2-116">Thread safety</span></span>

<span data-ttu-id="27fa2-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="27fa2-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="27fa2-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="27fa2-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="27fa2-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="27fa2-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="27fa2-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="27fa2-120">Reference</span></span>

[<span data-ttu-id="27fa2-121">Membri di EsentLogWriteFailException</span><span class="sxs-lookup"><span data-stu-id="27fa2-121">EsentLogWriteFailException members</span></span>](./esentlogwritefailexception-members.md)

[<span data-ttu-id="27fa2-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="27fa2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
