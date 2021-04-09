---
description: 'Altre informazioni su: classe EsentErrorException'
title: Classe EsentErrorException
TOCTitle: EsentErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception(v=EXCHG.10)
ms:contentKeyID: 55101648
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: eb05197392c1d5c8798968254b24d2d0ae677bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050228"
---
# <a name="esenterrorexception-class"></a><span data-ttu-id="0b470-103">Classe EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0b470-103">EsentErrorException class</span></span>

<span data-ttu-id="0b470-104">Classe di base per le eccezioni di errore ESENT.</span><span class="sxs-lookup"><span data-stu-id="0b470-104">Base class for ESENT error exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="0b470-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="0b470-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="0b470-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="0b470-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="0b470-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="0b470-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="0b470-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="0b470-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      <span data-ttu-id="0b470-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0b470-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>  
        [<span data-ttu-id="0b470-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="0b470-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
        [<span data-ttu-id="0b470-111">Microsoft. ISAM. esent. Interop. EsentCannotLogDuringRecoveryRedoException</span><span class="sxs-lookup"><span data-stu-id="0b470-111">Microsoft.Isam.Esent.Interop.EsentCannotLogDuringRecoveryRedoException</span></span>](./esentcannotlogduringrecoveryredoexception-class.md)  
        [<span data-ttu-id="0b470-112">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="0b470-112">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
        [<span data-ttu-id="0b470-113">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="0b470-113">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
        [<span data-ttu-id="0b470-114">Microsoft. ISAM. esent. Interop. EsentPreviousVersionException</span><span class="sxs-lookup"><span data-stu-id="0b470-114">Microsoft.Isam.Esent.Interop.EsentPreviousVersionException</span></span>](./esentpreviousversionexception-class.md)  
        [<span data-ttu-id="0b470-115">Microsoft. ISAM. esent. Interop. EsentVersionStoreEntryTooBigException</span><span class="sxs-lookup"><span data-stu-id="0b470-115">Microsoft.Isam.Esent.Interop.EsentVersionStoreEntryTooBigException</span></span>](./esentversionstoreentrytoobigexception-class.md)  

<span data-ttu-id="0b470-116">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b470-116">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b470-117">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b470-117">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b470-118">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b470-118">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Class EsentErrorException _
    Inherits EsentException
'Usage
Dim instance As EsentErrorException
```

``` csharp
[SerializableAttribute]
public class EsentErrorException : EsentException
```

## <a name="thread-safety"></a><span data-ttu-id="0b470-119">Thread safety</span><span class="sxs-lookup"><span data-stu-id="0b470-119">Thread safety</span></span>

<span data-ttu-id="0b470-120">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="0b470-120">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="0b470-121">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0b470-121">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b470-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0b470-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b470-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0b470-123">Reference</span></span>

[<span data-ttu-id="0b470-124">Membri di EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="0b470-124">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="0b470-125">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0b470-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
