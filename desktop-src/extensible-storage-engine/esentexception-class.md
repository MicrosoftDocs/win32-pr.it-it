---
description: 'Altre informazioni su: classe EsentException'
title: Classe EsentException (Microsoft. ISAM. ESENT)
TOCTitle: EsentException class
ms:assetid: T:Microsoft.Isam.Esent.EsentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100645
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.EsentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.EsentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 775d63c6b1d234696790b1187538a6d1ee734a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318451"
---
# <a name="esentexception-class"></a><span data-ttu-id="19632-103">Classe EsentException</span><span class="sxs-lookup"><span data-stu-id="19632-103">EsentException class</span></span>

<span data-ttu-id="19632-104">Classe di base per le eccezioni ESENT.</span><span class="sxs-lookup"><span data-stu-id="19632-104">Base class for ESENT exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="19632-105">Gerarchia di ereditarietà</span><span class="sxs-lookup"><span data-stu-id="19632-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="19632-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="19632-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="19632-107">System. Exception</span><span class="sxs-lookup"><span data-stu-id="19632-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    <span data-ttu-id="19632-108">Microsoft. ISAM. esent. EsentException</span><span class="sxs-lookup"><span data-stu-id="19632-108">Microsoft.Isam.Esent.EsentException</span></span>  
      [<span data-ttu-id="19632-109">Microsoft. ISAM. esent. Interop. EsentErrorException</span><span class="sxs-lookup"><span data-stu-id="19632-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
      [<span data-ttu-id="19632-110">Microsoft. ISAM. esent. Interop. EsentInvalidColumnException</span><span class="sxs-lookup"><span data-stu-id="19632-110">Microsoft.Isam.Esent.Interop.EsentInvalidColumnException</span></span>](./esentinvalidcolumnexception-class.md)  

<span data-ttu-id="19632-111">**Spazio dei nomi:**  [Microsoft. ISAM. ESENT](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="19632-111">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="19632-112">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="19632-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="19632-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19632-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentException _
    Inherits Exception
'Usage
Dim instance As EsentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentException : Exception
```

## <a name="thread-safety"></a><span data-ttu-id="19632-114">Thread safety</span><span class="sxs-lookup"><span data-stu-id="19632-114">Thread safety</span></span>

<span data-ttu-id="19632-115">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="19632-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="19632-116">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="19632-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="19632-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19632-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="19632-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="19632-118">Reference</span></span>

[<span data-ttu-id="19632-119">Membri di EsentException</span><span class="sxs-lookup"><span data-stu-id="19632-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="19632-120">Spazio dei nomi Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="19632-120">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
