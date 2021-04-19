---
description: 'Altre informazioni su: classe EsentTempPathInUseException'
title: Classe EsentTempPathInUseException
TOCTitle: EsentTempPathInUseException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTempPathInUseException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttemppathinuseexception(v=EXCHG.10)
ms:contentKeyID: 55103033
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTempPathInUseException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTempPathInUseException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0d18cea8af69eb3067e01bfa5c22a65f736698ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313578"
---
# <a name="esenttemppathinuseexception-class"></a><span data-ttu-id="a7536-103">Classe EsentTempPathInUseException</span><span class="sxs-lookup"><span data-stu-id="a7536-103">EsentTempPathInUseException class</span></span>

<span data-ttu-id="a7536-104">Classe di base per JET_err. Eccezioni TempPathInUse.</span><span class="sxs-lookup"><span data-stu-id="a7536-104">Base class for JET_err.TempPathInUse exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a7536-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="a7536-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a7536-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a7536-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a7536-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a7536-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a7536-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a7536-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a7536-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a7536-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a7536-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="a7536-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="a7536-111">Microsoft. ISAM. esent. Interop. EsentUsageException</span><span class="sxs-lookup"><span data-stu-id="a7536-111">Microsoft.Isam.Esent.Interop.EsentUsageException</span></span>](./esentusageexception-class.md)  
            <span data-ttu-id="a7536-112">Microsoft. ISAM. esent. Interop. EsentTempPathInUseException</span><span class="sxs-lookup"><span data-stu-id="a7536-112">Microsoft.Isam.Esent.Interop.EsentTempPathInUseException</span></span>  

<span data-ttu-id="a7536-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a7536-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a7536-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a7536-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7536-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7536-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTempPathInUseException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentTempPathInUseException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTempPathInUseException : EsentUsageException
```

## <a name="thread-safety"></a><span data-ttu-id="a7536-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="a7536-116">Thread safety</span></span>

<span data-ttu-id="a7536-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a7536-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a7536-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a7536-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7536-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7536-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7536-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a7536-120">Reference</span></span>

[<span data-ttu-id="a7536-121">Membri di EsentTempPathInUseException</span><span class="sxs-lookup"><span data-stu-id="a7536-121">EsentTempPathInUseException members</span></span>](./esenttemppathinuseexception-members.md)

[<span data-ttu-id="a7536-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a7536-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
