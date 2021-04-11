---
description: 'Altre informazioni su: classe EsentTooManyOpenDatabasesException'
title: Classe EsentTooManyOpenDatabasesException
TOCTitle: EsentTooManyOpenDatabasesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopendatabasesexception(v=EXCHG.10)
ms:contentKeyID: 55103102
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9df65671d3f93cc131d28beb18232e94cba505ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233384"
---
# <a name="esenttoomanyopendatabasesexception-class"></a><span data-ttu-id="8f78d-103">Classe EsentTooManyOpenDatabasesException</span><span class="sxs-lookup"><span data-stu-id="8f78d-103">EsentTooManyOpenDatabasesException class</span></span>

<span data-ttu-id="8f78d-104">Classe di base per JET_err. Eccezioni TooManyOpenDatabases.</span><span class="sxs-lookup"><span data-stu-id="8f78d-104">Base class for JET_err.TooManyOpenDatabases exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="8f78d-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="8f78d-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="8f78d-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="8f78d-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="8f78d-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="8f78d-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="8f78d-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="8f78d-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="8f78d-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="8f78d-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="8f78d-110">Microsoft. ISAM. esent. Interop. EsentApiException</span><span class="sxs-lookup"><span data-stu-id="8f78d-110">Microsoft.Isam.Esent.Interop.EsentApiException</span></span>](./esentapiexception-class.md)  
          [<span data-ttu-id="8f78d-111">Microsoft. ISAM. esent. Interop. EsentObsoleteException</span><span class="sxs-lookup"><span data-stu-id="8f78d-111">Microsoft.Isam.Esent.Interop.EsentObsoleteException</span></span>](./esentobsoleteexception-class.md)  
            <span data-ttu-id="8f78d-112">Microsoft. ISAM. esent. Interop. EsentTooManyOpenDatabasesException</span><span class="sxs-lookup"><span data-stu-id="8f78d-112">Microsoft.Isam.Esent.Interop.EsentTooManyOpenDatabasesException</span></span>  

<span data-ttu-id="8f78d-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8f78d-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8f78d-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8f78d-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8f78d-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8f78d-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenDatabasesException _
    Inherits EsentObsoleteException
'Usage
Dim instance As EsentTooManyOpenDatabasesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenDatabasesException : EsentObsoleteException
```

## <a name="thread-safety"></a><span data-ttu-id="8f78d-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="8f78d-116">Thread safety</span></span>

<span data-ttu-id="8f78d-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8f78d-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="8f78d-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="8f78d-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="8f78d-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8f78d-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8f78d-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8f78d-120">Reference</span></span>

[<span data-ttu-id="8f78d-121">Membri di EsentTooManyOpenDatabasesException</span><span class="sxs-lookup"><span data-stu-id="8f78d-121">EsentTooManyOpenDatabasesException members</span></span>](./esenttoomanyopendatabasesexception-members.md)

[<span data-ttu-id="8f78d-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8f78d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
