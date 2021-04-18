---
description: 'Altre informazioni su: classe EsentRollbackErrorException'
title: Classe EsentRollbackErrorException
TOCTitle: EsentRollbackErrorException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentrollbackerrorexception(v=EXCHG.10)
ms:contentKeyID: 55102663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentRollbackErrorException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6e56e3e829b8c44ff6325ed877606fb44471f6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309659"
---
# <a name="esentrollbackerrorexception-class"></a><span data-ttu-id="a56eb-103">Classe EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="a56eb-103">EsentRollbackErrorException class</span></span>

<span data-ttu-id="a56eb-104">Classe di base per JET_err. Eccezioni RollbackError.</span><span class="sxs-lookup"><span data-stu-id="a56eb-104">Base class for JET_err.RollbackError exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="a56eb-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="a56eb-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="a56eb-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="a56eb-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="a56eb-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="a56eb-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="a56eb-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="a56eb-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="a56eb-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="a56eb-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        [<span data-ttu-id="a56eb-110">Microsoft. ISAM. esent. Interop. EsentOperationException</span><span class="sxs-lookup"><span data-stu-id="a56eb-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>](./esentoperationexception-class.md)  
          [<span data-ttu-id="a56eb-111">Microsoft. ISAM. esent. Interop. EsentFatalException</span><span class="sxs-lookup"><span data-stu-id="a56eb-111">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
            <span data-ttu-id="a56eb-112">Microsoft. ISAM. esent. Interop. EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="a56eb-112">Microsoft.Isam.Esent.Interop.EsentRollbackErrorException</span></span>  

<span data-ttu-id="a56eb-113">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a56eb-113">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a56eb-114">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a56eb-114">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a56eb-115">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a56eb-115">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentRollbackErrorException _
    Inherits EsentFatalException
'Usage
Dim instance As EsentRollbackErrorException
```

``` csharp
[SerializableAttribute]
public sealed class EsentRollbackErrorException : EsentFatalException
```

## <a name="thread-safety"></a><span data-ttu-id="a56eb-116">Thread safety</span><span class="sxs-lookup"><span data-stu-id="a56eb-116">Thread safety</span></span>

<span data-ttu-id="a56eb-117">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="a56eb-117">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="a56eb-118">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a56eb-118">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="a56eb-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a56eb-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a56eb-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a56eb-120">Reference</span></span>

[<span data-ttu-id="a56eb-121">Membri di EsentRollbackErrorException</span><span class="sxs-lookup"><span data-stu-id="a56eb-121">EsentRollbackErrorException members</span></span>](./esentrollbackerrorexception-members.md)

[<span data-ttu-id="a56eb-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a56eb-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
