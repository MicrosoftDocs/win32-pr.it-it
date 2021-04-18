---
description: 'Altre informazioni su: struttura JET_THREADSTATS'
title: Struttura JET_THREADSTATS (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: JET_THREADSTATS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats(v=EXCHG.10)
ms:contentKeyID: 39512342
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 764a9276543fbb7a5b1aa2762cc8ed1877c45ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305745"
---
# <a name="jet_threadstats-structure"></a><span data-ttu-id="84800-103">Struttura JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="84800-103">JET_THREADSTATS structure</span></span>

<span data-ttu-id="84800-104">Contiene statistiche cumulative sul lavoro eseguito dal motore di database sul thread corrente.</span><span class="sxs-lookup"><span data-stu-id="84800-104">Contains cumulative statistics on the work performed by the database engine on the current thread.</span></span> <span data-ttu-id="84800-105">Queste informazioni vengono restituite tramite JetGetThreadStats.</span><span class="sxs-lookup"><span data-stu-id="84800-105">This information is returned via JetGetThreadStats.</span></span>

<span data-ttu-id="84800-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="84800-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="84800-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="84800-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="84800-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84800-108">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_THREADSTATS _
    Implements IEquatable(Of JET_THREADSTATS)
'Usage
Dim instance As JET_THREADSTATS
```

``` csharp
[SerializableAttribute]
public struct JET_THREADSTATS : IEquatable<JET_THREADSTATS>
```

## <a name="thread-safety"></a><span data-ttu-id="84800-109">Thread safety</span><span class="sxs-lookup"><span data-stu-id="84800-109">Thread safety</span></span>

<span data-ttu-id="84800-110">I membri statici pubblici (Shared in Visual Basic) di questo tipo sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="84800-110">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="84800-111">Non è invece garantita la sicurezza dei membri dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="84800-111">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="84800-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84800-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="84800-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="84800-113">Reference</span></span>

[<span data-ttu-id="84800-114">Membri JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="84800-114">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="84800-115">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="84800-115">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
