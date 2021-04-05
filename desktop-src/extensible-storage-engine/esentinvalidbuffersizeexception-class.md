---
description: 'Altre informazioni su: classe EsentInvalidBufferSizeException'
title: Classe EsentInvalidBufferSizeException
TOCTitle: EsentInvalidBufferSizeException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentinvalidbuffersizeexception(v=EXCHG.10)
ms:contentKeyID: 55101912
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0dc693135124ba5d2979fa0f1a7ff80fcca27600
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882597"
---
# <a name="esentinvalidbuffersizeexception-class"></a><span data-ttu-id="47a52-103">Classe EsentInvalidBufferSizeException</span><span class="sxs-lookup"><span data-stu-id="47a52-103">EsentInvalidBufferSizeException class</span></span>

<span data-ttu-id="47a52-104">Classe di base per JET_err. Eccezioni InvalidBufferSize.</span><span class="sxs-lookup"><span data-stu-id="47a52-104">Base class for JET_err.InvalidBufferSize exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="47a52-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="47a52-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="47a52-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="47a52-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="47a52-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="47a52-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="47a52-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="47a52-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="47a52-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="47a52-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="47a52-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="47a52-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="47a52-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="47a52-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="47a52-112">Microsoft. ISAM. esent. Interop. EsentInvalidBufferSizeException</span><span class="sxs-lookup"><span data-stu-id="47a52-112">Microsoft.Isam.Esent.Interop.EsentInvalidBufferSizeException</span></span>  

<span data-ttu-id="47a52-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="47a52-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="47a52-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="47a52-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="47a52-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47a52-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentInvalidBufferSizeException _
    Inherits EsentStateException
'Usage
Dim instance As EsentInvalidBufferSizeException
```

``` csharp
[SerializableAttribute]
public sealed class EsentInvalidBufferSizeException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="47a52-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="47a52-116">Thread safety</span></span>

<span data-ttu-id="47a52-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="47a52-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="47a52-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="47a52-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="47a52-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="47a52-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="47a52-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="47a52-120">Reference</span></span>

[<span data-ttu-id="47a52-121">Membri di EsentInvalidBufferSizeException</span><span class="sxs-lookup"><span data-stu-id="47a52-121">EsentInvalidBufferSizeException members</span></span>](./esentinvalidbuffersizeexception-members.md)

[<span data-ttu-id="47a52-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="47a52-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
