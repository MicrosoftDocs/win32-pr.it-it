---
description: 'Altre informazioni su: classe EsentBackupInProgressException'
title: Classe EsentBackupInProgressException
TOCTitle: EsentBackupInProgressException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupInProgressException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupinprogressexception(v=EXCHG.10)
ms:contentKeyID: 55101081
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupInProgressException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupInProgressException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cae492abaaeac2b4f21b2afd109f8504fdc663f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349181"
---
# <a name="esentbackupinprogressexception-class"></a><span data-ttu-id="4bc51-103">Classe EsentBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="4bc51-103">EsentBackupInProgressException class</span></span>

<span data-ttu-id="4bc51-104">Classe di base per JET_err. Eccezioni BackupInProgress.</span><span class="sxs-lookup"><span data-stu-id="4bc51-104">Base class for JET_err.BackupInProgress exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4bc51-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="4bc51-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4bc51-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4bc51-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4bc51-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4bc51-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4bc51-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="4bc51-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4bc51-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="4bc51-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4bc51-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="4bc51-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4bc51-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="4bc51-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="4bc51-112">Microsoft. ISAM. esent. Interop. EsentBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="4bc51-112">Microsoft.Isam.Esent.Interop.EsentBackupInProgressException</span></span>  

<span data-ttu-id="4bc51-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4bc51-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4bc51-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4bc51-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4bc51-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bc51-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupInProgressException _
    Inherits EsentStateException
'Usage
Dim instance As EsentBackupInProgressException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupInProgressException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="4bc51-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="4bc51-116">Thread safety</span></span>

<span data-ttu-id="4bc51-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4bc51-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4bc51-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="4bc51-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bc51-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bc51-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4bc51-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4bc51-120">Reference</span></span>

[<span data-ttu-id="4bc51-121">Membri di EsentBackupInProgressException</span><span class="sxs-lookup"><span data-stu-id="4bc51-121">EsentBackupInProgressException members</span></span>](./esentbackupinprogressexception-members.md)

[<span data-ttu-id="4bc51-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4bc51-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
