---
description: 'Altre informazioni su: classe EsentTooManyOpenTablesException'
title: Classe EsentTooManyOpenTablesException
TOCTitle: EsentTooManyOpenTablesException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenttoomanyopentablesexception(v=EXCHG.10)
ms:contentKeyID: 55107362
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 066191af07aab606731f98a16369b2500d24cda6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130570"
---
# <a name="esenttoomanyopentablesexception-class"></a><span data-ttu-id="e4ba3-103">Classe EsentTooManyOpenTablesException</span><span class="sxs-lookup"><span data-stu-id="e4ba3-103">EsentTooManyOpenTablesException class</span></span>

<span data-ttu-id="e4ba3-104">Classe di base per JET_err. Eccezioni TooManyOpenTables.</span><span class="sxs-lookup"><span data-stu-id="e4ba3-104">Base class for JET_err.TooManyOpenTables exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="e4ba3-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="e4ba3-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="e4ba3-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="e4ba3-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="e4ba3-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="e4ba3-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="e4ba3-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="e4ba3-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="e4ba3-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="e4ba3-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="e4ba3-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="e4ba3-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="e4ba3-111">Microsoft. ISAM. esent. Interop. EsentResourceException</span><span class="sxs-lookup"><span data-stu-id="e4ba3-111">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
            [<span data-ttu-id="e4ba3-112">Microsoft. ISAM. esent. Interop. EsentQuotaException</span><span class="sxs-lookup"><span data-stu-id="e4ba3-112">Microsoft.Isam.Esent.Interop.EsentQuotaException</span></span>](./esentquotaexception-class.md)  
              <span data-ttu-id="e4ba3-113">Microsoft. ISAM. esent. Interop. EsentTooManyOpenTablesException</span><span class="sxs-lookup"><span data-stu-id="e4ba3-113">Microsoft.Isam.Esent.Interop.EsentTooManyOpenTablesException</span></span>  

<span data-ttu-id="e4ba3-114">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4ba3-114">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e4ba3-115">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e4ba3-115">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ba3-116">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4ba3-116">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentTooManyOpenTablesException _
    Inherits EsentQuotaException
'Usage
Dim instance As EsentTooManyOpenTablesException
```

``` csharp
[SerializableAttribute]
public sealed class EsentTooManyOpenTablesException : EsentQuotaException
```

## <a name="thread-safety"></a><span data-ttu-id="e4ba3-117">Thread safety</span><span class="sxs-lookup"><span data-stu-id="e4ba3-117">Thread safety</span></span>

<span data-ttu-id="e4ba3-118">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="e4ba3-118">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="e4ba3-119">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e4ba3-119">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4ba3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4ba3-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4ba3-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e4ba3-121">Reference</span></span>

[<span data-ttu-id="e4ba3-122">Membri di EsentTooManyOpenTablesException</span><span class="sxs-lookup"><span data-stu-id="e4ba3-122">EsentTooManyOpenTablesException members</span></span>](./esenttoomanyopentablesexception-members.md)

[<span data-ttu-id="e4ba3-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e4ba3-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
