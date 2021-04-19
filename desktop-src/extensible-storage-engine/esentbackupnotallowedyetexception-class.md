---
description: 'Altre informazioni su: classe EsentBackupNotAllowedYetException'
title: Classe EsentBackupNotAllowedYetException
TOCTitle: EsentBackupNotAllowedYetException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentbackupnotallowedyetexception(v=EXCHG.10)
ms:contentKeyID: 55101088
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5481c51c4a0b78ea1b66b950ac53d2a04c28595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317507"
---
# <a name="esentbackupnotallowedyetexception-class"></a><span data-ttu-id="069f0-103">Classe EsentBackupNotAllowedYetException</span><span class="sxs-lookup"><span data-stu-id="069f0-103">EsentBackupNotAllowedYetException class</span></span>

<span data-ttu-id="069f0-104">Classe di base per JET_err. Eccezioni BackupNotAllowedYet.</span><span class="sxs-lookup"><span data-stu-id="069f0-104">Base class for JET_err.BackupNotAllowedYet exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="069f0-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="069f0-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="069f0-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="069f0-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="069f0-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="069f0-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="069f0-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="069f0-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="069f0-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="069f0-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="069f0-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="069f0-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="069f0-111">Microsoft. ISAM. esent. Interop. EsentStateException</span><span class="sxs-lookup"><span data-stu-id="069f0-111">Microsoft.Isam.Esent.Interop.EsentStateException</span></span>](./esentstateexception-class.md)  
            <span data-ttu-id="069f0-112">Microsoft. ISAM. esent. Interop. EsentBackupNotAllowedYetException</span><span class="sxs-lookup"><span data-stu-id="069f0-112">Microsoft.Isam.Esent.Interop.EsentBackupNotAllowedYetException</span></span>  

<span data-ttu-id="069f0-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="069f0-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="069f0-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="069f0-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="069f0-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="069f0-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentBackupNotAllowedYetException _
    Inherits EsentStateException
'Usage
Dim instance As EsentBackupNotAllowedYetException
```

``` csharp
[SerializableAttribute]
public sealed class EsentBackupNotAllowedYetException : EsentStateException
```

## <a name="thread-safety"></a><span data-ttu-id="069f0-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="069f0-116">Thread safety</span></span>

<span data-ttu-id="069f0-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="069f0-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="069f0-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="069f0-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="069f0-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="069f0-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="069f0-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="069f0-120">Reference</span></span>

[<span data-ttu-id="069f0-121">Membri di EsentBackupNotAllowedYetException</span><span class="sxs-lookup"><span data-stu-id="069f0-121">EsentBackupNotAllowedYetException members</span></span>](./esentbackupnotallowedyetexception-members.md)

[<span data-ttu-id="069f0-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="069f0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
