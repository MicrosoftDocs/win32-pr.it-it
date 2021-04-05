---
description: 'Altre informazioni su: classe EsentMissingFullBackupException'
title: Classe EsentMissingFullBackupException
TOCTitle: EsentMissingFullBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingfullbackupexception(v=EXCHG.10)
ms:contentKeyID: 55102230
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c345475e9e23f60460d7ee5eb901e5997ecb6062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130883"
---
# <a name="esentmissingfullbackupexception-class"></a><span data-ttu-id="53dc5-103">Classe EsentMissingFullBackupException</span><span class="sxs-lookup"><span data-stu-id="53dc5-103">EsentMissingFullBackupException class</span></span>

<span data-ttu-id="53dc5-104">Classe di base per JET_err. Eccezioni MissingFullBackup.</span><span class="sxs-lookup"><span data-stu-id="53dc5-104">Base class for JET_err.MissingFullBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="53dc5-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="53dc5-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="53dc5-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="53dc5-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="53dc5-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="53dc5-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="53dc5-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="53dc5-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="53dc5-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="53dc5-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="53dc5-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="53dc5-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="53dc5-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="53dc5-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="53dc5-112">Microsoft. ISAM. esent. Interop. EsentMissingFullBackupException</span><span class="sxs-lookup"><span data-stu-id="53dc5-112">Microsoft.Isam.Esent.Interop.EsentMissingFullBackupException</span></span>  

<span data-ttu-id="53dc5-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="53dc5-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="53dc5-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="53dc5-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="53dc5-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53dc5-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingFullBackupException _
    Inherits EsentStateException
'Usage
Dim instance As EsentMissingFullBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingFullBackupException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="53dc5-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="53dc5-116">Thread safety</span></span>

<span data-ttu-id="53dc5-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="53dc5-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="53dc5-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="53dc5-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="53dc5-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53dc5-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="53dc5-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="53dc5-120">Reference</span></span>

[<span data-ttu-id="53dc5-121">Membri di EsentMissingFullBackupException</span><span class="sxs-lookup"><span data-stu-id="53dc5-121">EsentMissingFullBackupException members</span></span>](./esentmissingfullbackupexception-members.md)

[<span data-ttu-id="53dc5-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="53dc5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
