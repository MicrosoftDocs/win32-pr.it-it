---
description: 'Altre informazioni su: JET_INSTANCE. Operatore di uguaglianza'
title: JET_INSTANCE. Operatore di uguaglianza
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41a3ffe2eebeb7566d431c655a27360c9380413c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313122"
---
# <a name="jet_instanceequality-operator"></a><span data-ttu-id="33e1f-103">JET_INSTANCE. Operatore di uguaglianza</span><span class="sxs-lookup"><span data-stu-id="33e1f-103">JET_INSTANCE.Equality operator</span></span>

<span data-ttu-id="33e1f-104">Determina se due istanze specificate di JET_INSTANCE sono uguali.</span><span class="sxs-lookup"><span data-stu-id="33e1f-104">Determines whether two specified instances of JET_INSTANCE are equal.</span></span>

<span data-ttu-id="33e1f-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="33e1f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="33e1f-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="33e1f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="33e1f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33e1f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="33e1f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="33e1f-108">Parameters</span></span>

  - <span data-ttu-id="33e1f-109">LHS</span><span class="sxs-lookup"><span data-stu-id="33e1f-109">lhs</span></span>  
    <span data-ttu-id="33e1f-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="33e1f-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="33e1f-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="33e1f-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="33e1f-112">rhs</span><span class="sxs-lookup"><span data-stu-id="33e1f-112">rhs</span></span>  
    <span data-ttu-id="33e1f-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="33e1f-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="33e1f-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="33e1f-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="33e1f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33e1f-115">Return value</span></span>

<span data-ttu-id="33e1f-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="33e1f-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="33e1f-117">True se le due istanze sono uguali.</span><span class="sxs-lookup"><span data-stu-id="33e1f-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="33e1f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33e1f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="33e1f-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="33e1f-119">Reference</span></span>

[<span data-ttu-id="33e1f-120">Struttura JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="33e1f-120">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="33e1f-121">Membri JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="33e1f-121">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="33e1f-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="33e1f-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
