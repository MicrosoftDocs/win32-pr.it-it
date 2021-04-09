---
description: 'Altre informazioni su: classe EsentNotInDistributedTransactionException'
title: Classe EsentNotInDistributedTransactionException
TOCTitle: EsentNotInDistributedTransactionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnotindistributedtransactionexception(v=EXCHG.10)
ms:contentKeyID: 55102293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 983aa045b83a0382a3ec7676080f3cdada5e1517
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968637"
---
# <a name="esentnotindistributedtransactionexception-class"></a><span data-ttu-id="34e92-103">Classe EsentNotInDistributedTransactionException</span><span class="sxs-lookup"><span data-stu-id="34e92-103">EsentNotInDistributedTransactionException class</span></span>

<span data-ttu-id="34e92-104">Classe di base per JET_err. Eccezioni NotInDistributedTransaction.</span><span class="sxs-lookup"><span data-stu-id="34e92-104">Base class for JET_err.NotInDistributedTransaction exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="34e92-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="34e92-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="34e92-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="34e92-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="34e92-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="34e92-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="34e92-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="34e92-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="34e92-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="34e92-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="34e92-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="34e92-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="34e92-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="34e92-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="34e92-112">Microsoft. ISAM. esent. Interop. EsentNotInDistributedTransactionException</span><span class="sxs-lookup"><span data-stu-id="34e92-112">Microsoft.Isam.Esent.Interop.EsentNotInDistributedTransactionException</span></span>  

<span data-ttu-id="34e92-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="34e92-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="34e92-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="34e92-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="34e92-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34e92-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNotInDistributedTransactionException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentNotInDistributedTransactionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNotInDistributedTransactionException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="34e92-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="34e92-116">Thread safety</span></span>

<span data-ttu-id="34e92-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="34e92-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="34e92-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="34e92-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="34e92-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34e92-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="34e92-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="34e92-120">Reference</span></span>

[<span data-ttu-id="34e92-121">Membri di EsentNotInDistributedTransactionException</span><span class="sxs-lookup"><span data-stu-id="34e92-121">EsentNotInDistributedTransactionException members</span></span>](./esentnotindistributedtransactionexception-members.md)

[<span data-ttu-id="34e92-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="34e92-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
