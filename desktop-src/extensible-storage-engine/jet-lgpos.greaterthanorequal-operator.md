---
description: 'Altre informazioni su: JET_LGPOS. Operatore GreaterThanOrEqual'
title: JET_LGPOS. Operatore GreaterThanOrEqual
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510730
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a932ea983b3044d1db8395fbf87962cd3b733ae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319663"
---
# <a name="jet_lgposgreaterthanorequal-operator"></a><span data-ttu-id="33068-103">JET_LGPOS. Operatore GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="33068-103">JET_LGPOS.GreaterThanOrEqual operator</span></span>

<span data-ttu-id="33068-104">Determinare se una posizione del log è successiva o uguale a un'altra posizione del log.</span><span class="sxs-lookup"><span data-stu-id="33068-104">Determine whether one log position is after or equal to another log position.</span></span>

<span data-ttu-id="33068-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="33068-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="33068-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="33068-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="33068-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33068-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="33068-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="33068-108">Parameters</span></span>

  - <span data-ttu-id="33068-109">LHS</span><span class="sxs-lookup"><span data-stu-id="33068-109">lhs</span></span>  
    <span data-ttu-id="33068-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="33068-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="33068-111">Prima posizione del log da confrontare.</span><span class="sxs-lookup"><span data-stu-id="33068-111">The first log position to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="33068-112">rhs</span><span class="sxs-lookup"><span data-stu-id="33068-112">rhs</span></span>  
    <span data-ttu-id="33068-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="33068-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="33068-114">Seconda posizione del log da confrontare.</span><span class="sxs-lookup"><span data-stu-id="33068-114">The second log position to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="33068-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33068-115">Return value</span></span>

<span data-ttu-id="33068-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="33068-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="33068-117">True se LHS viene seguito o è uguale a RHS.</span><span class="sxs-lookup"><span data-stu-id="33068-117">True if lhs comes after or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="33068-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33068-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="33068-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="33068-119">Reference</span></span>

[<span data-ttu-id="33068-120">Struttura JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="33068-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="33068-121">Membri JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="33068-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="33068-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="33068-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
