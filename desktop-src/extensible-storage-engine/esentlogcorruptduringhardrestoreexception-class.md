---
description: 'Altre informazioni su: classe EsentLogCorruptDuringHardRestoreException'
title: Classe EsentLogCorruptDuringHardRestoreException
TOCTitle: EsentLogCorruptDuringHardRestoreException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptduringhardrestoreexception(v=EXCHG.10)
ms:contentKeyID: 55102073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: daeabeae72916781e01640cd0de10c737b53e5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233912"
---
# <a name="esentlogcorruptduringhardrestoreexception-class"></a><span data-ttu-id="9873e-103">Classe EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="9873e-103">EsentLogCorruptDuringHardRestoreException class</span></span>

<span data-ttu-id="9873e-104">Classe di base per JET_err. Eccezioni LogCorruptDuringHardRestore.</span><span class="sxs-lookup"><span data-stu-id="9873e-104">Base class for JET_err.LogCorruptDuringHardRestore exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="9873e-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="9873e-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="9873e-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="9873e-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="9873e-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="9873e-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="9873e-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="9873e-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="9873e-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="9873e-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="9873e-110">Microsoft. ISAM. esent. Interop. EsentDataException</span><span class="sxs-lookup"><span data-stu-id="9873e-110">Microsoft.Isam.Esent.Interop.EsentDataException</span></span>](./esentdataexception-class.md)  
          [<span data-ttu-id="9873e-111">Microsoft. ISAM. esent. Interop. EsentCorruptionException</span><span class="sxs-lookup"><span data-stu-id="9873e-111">Microsoft.Isam.Esent.Interop.EsentCorruptionException</span></span>](./esentcorruptionexception-class.md)  
            <span data-ttu-id="9873e-112">Microsoft. ISAM. esent. Interop. EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="9873e-112">Microsoft.Isam.Esent.Interop.EsentLogCorruptDuringHardRestoreException</span></span>  

<span data-ttu-id="9873e-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9873e-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9873e-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9873e-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9873e-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9873e-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptDuringHardRestoreException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptDuringHardRestoreException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptDuringHardRestoreException : EsentCorruptionException
```

## <a name="thread-safety"></a><span data-ttu-id="9873e-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="9873e-116">Thread safety</span></span>

<span data-ttu-id="9873e-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="9873e-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="9873e-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="9873e-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="9873e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9873e-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9873e-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9873e-120">Reference</span></span>

[<span data-ttu-id="9873e-121">Membri di EsentLogCorruptDuringHardRestoreException</span><span class="sxs-lookup"><span data-stu-id="9873e-121">EsentLogCorruptDuringHardRestoreException members</span></span>](./esentlogcorruptduringhardrestoreexception-members.md)

[<span data-ttu-id="9873e-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9873e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
