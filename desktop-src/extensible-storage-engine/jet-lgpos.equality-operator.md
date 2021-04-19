---
description: 'Altre informazioni su: JET_LGPOS. Operatore di uguaglianza'
title: JET_LGPOS. Operatore di uguaglianza
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Equality(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_equality(v=EXCHG.10)
ms:contentKeyID: 39510144
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Equality
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ffdde1ee34cb60761d55dd52f2145a6b9bdd0a79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319666"
---
# <a name="jet_lgposequality-operator"></a><span data-ttu-id="07830-103">JET_LGPOS. Operatore di uguaglianza</span><span class="sxs-lookup"><span data-stu-id="07830-103">JET_LGPOS.Equality operator</span></span>

<span data-ttu-id="07830-104">Determina se due istanze specificate di JET_LGPOS sono uguali.</span><span class="sxs-lookup"><span data-stu-id="07830-104">Determines whether two specified instances of JET_LGPOS are equal.</span></span>

<span data-ttu-id="07830-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="07830-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="07830-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="07830-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="07830-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07830-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="07830-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="07830-108">Parameters</span></span>

  - <span data-ttu-id="07830-109">LHS</span><span class="sxs-lookup"><span data-stu-id="07830-109">lhs</span></span>  
    <span data-ttu-id="07830-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="07830-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="07830-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="07830-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="07830-112">rhs</span><span class="sxs-lookup"><span data-stu-id="07830-112">rhs</span></span>  
    <span data-ttu-id="07830-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="07830-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="07830-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="07830-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="07830-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07830-115">Return value</span></span>

<span data-ttu-id="07830-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="07830-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="07830-117">True se le due istanze sono uguali.</span><span class="sxs-lookup"><span data-stu-id="07830-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="07830-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07830-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="07830-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="07830-119">Reference</span></span>

[<span data-ttu-id="07830-120">Struttura JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="07830-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="07830-121">Membri JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="07830-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="07830-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="07830-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
