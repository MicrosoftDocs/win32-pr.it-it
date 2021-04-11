---
description: 'Altre informazioni su: classe EsentDatabaseUnavailableException'
title: Classe EsentDatabaseUnavailableException
TOCTitle: EsentDatabaseUnavailableException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdatabaseunavailableexception(v=EXCHG.10)
ms:contentKeyID: 55101562
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3210a3d5a546d6c27294473137b0306f87f0888
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226777"
---
# <a name="esentdatabaseunavailableexception-class"></a><span data-ttu-id="4178d-103">Classe EsentDatabaseUnavailableException</span><span class="sxs-lookup"><span data-stu-id="4178d-103">EsentDatabaseUnavailableException class</span></span>

<span data-ttu-id="4178d-104">Classe di base per JET_err. Eccezioni DatabaseUnavailable.</span><span class="sxs-lookup"><span data-stu-id="4178d-104">Base class for JET_err.DatabaseUnavailable exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="4178d-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="4178d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="4178d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="4178d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="4178d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="4178d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="4178d-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="4178d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="4178d-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="4178d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="4178d-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="4178d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="4178d-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="4178d-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="4178d-112">Microsoft. ISAM. esent. Interop. EsentDatabaseUnavailableException</span><span class="sxs-lookup"><span data-stu-id="4178d-112">Microsoft.Isam.Esent.Interop.EsentDatabaseUnavailableException</span></span>  

<span data-ttu-id="4178d-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4178d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4178d-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4178d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4178d-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4178d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDatabaseUnavailableException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentDatabaseUnavailableException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDatabaseUnavailableException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="4178d-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="4178d-116">Thread safety</span></span>

<span data-ttu-id="4178d-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="4178d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="4178d-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="4178d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="4178d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4178d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4178d-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4178d-120">Reference</span></span>

[<span data-ttu-id="4178d-121">Membri di EsentDatabaseUnavailableException</span><span class="sxs-lookup"><span data-stu-id="4178d-121">EsentDatabaseUnavailableException members</span></span>](./esentdatabaseunavailableexception-members.md)

[<span data-ttu-id="4178d-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4178d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
