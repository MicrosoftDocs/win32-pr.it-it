---
description: 'Altre informazioni su: classe EsentMissingFileToBackupException'
title: Classe EsentMissingFileToBackupException
TOCTitle: EsentMissingFileToBackupException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmissingfiletobackupexception(v=EXCHG.10)
ms:contentKeyID: 55102216
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5941140df070abb3a273378f3ec275eaf1c6fdd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226740"
---
# <a name="esentmissingfiletobackupexception-class"></a><span data-ttu-id="6a472-103">Classe EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="6a472-103">EsentMissingFileToBackupException class</span></span>

<span data-ttu-id="6a472-104">Classe di base per JET_err. Eccezioni MissingFileToBackup.</span><span class="sxs-lookup"><span data-stu-id="6a472-104">Base class for JET_err.MissingFileToBackup exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="6a472-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="6a472-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="6a472-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="6a472-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="6a472-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="6a472-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="6a472-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="6a472-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="6a472-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="6a472-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="6a472-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="6a472-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="6a472-111">Microsoft. ISAM. esent. Interop. EsentInconsistentException</span><span class="sxs-lookup"><span data-stu-id="6a472-111">Microsoft.Isam.Esent.Interop.EsentInconsistentException</span></span>](./esentinconsistentexception-class.md)  
            <span data-ttu-id="6a472-112">Microsoft. ISAM. esent. Interop. EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="6a472-112">Microsoft.Isam.Esent.Interop.EsentMissingFileToBackupException</span></span>  

<span data-ttu-id="6a472-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6a472-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6a472-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6a472-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6a472-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a472-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentMissingFileToBackupException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentMissingFileToBackupException
```

``` csharp
[SerializableAttribute]
public sealed class EsentMissingFileToBackupException : EsentInconsistentException
```

## <a name="thread-safety"></a><span data-ttu-id="6a472-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="6a472-116">Thread safety</span></span>

<span data-ttu-id="6a472-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="6a472-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="6a472-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="6a472-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a472-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a472-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6a472-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6a472-120">Reference</span></span>

[<span data-ttu-id="6a472-121">Membri di EsentMissingFileToBackupException</span><span class="sxs-lookup"><span data-stu-id="6a472-121">EsentMissingFileToBackupException members</span></span>](./esentmissingfiletobackupexception-members.md)

[<span data-ttu-id="6a472-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6a472-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
