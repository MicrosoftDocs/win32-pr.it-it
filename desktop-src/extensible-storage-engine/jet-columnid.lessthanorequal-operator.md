---
description: 'Altre informazioni su: JET_COLUMNID. Operatore LessThanOrEqual'
title: JET_COLUMNID. Operatore LessThanOrEqual
TOCTitle: 'LessThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthanorequal(v=EXCHG.10)
ms:contentKeyID: 39513688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9d6f98c5861a57fa4916ebca1b421c538d752d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753263"
---
# <a name="jet_columnidlessthanorequal-operator"></a><span data-ttu-id="89c67-103">JET_COLUMNID. Operatore LessThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="89c67-103">JET_COLUMNID.LessThanOrEqual operator</span></span>

<span data-ttu-id="89c67-104">Determinare se un columnid è precedente o uguale a un altro ColumnID.</span><span class="sxs-lookup"><span data-stu-id="89c67-104">Determine whether one columnid is before or equal to another columnid.</span></span>

<span data-ttu-id="89c67-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="89c67-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="89c67-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="89c67-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="89c67-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89c67-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <= ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <= rhs)
```

``` csharp
public static bool operator <=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="89c67-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89c67-108">Parameters</span></span>

  - <span data-ttu-id="89c67-109">LHS</span><span class="sxs-lookup"><span data-stu-id="89c67-109">lhs</span></span>  
    <span data-ttu-id="89c67-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="89c67-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="89c67-111">Primo ColumnID da confrontare.</span><span class="sxs-lookup"><span data-stu-id="89c67-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="89c67-112">rhs</span><span class="sxs-lookup"><span data-stu-id="89c67-112">rhs</span></span>  
    <span data-ttu-id="89c67-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="89c67-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="89c67-114">Secondo ColumnID da confrontare.</span><span class="sxs-lookup"><span data-stu-id="89c67-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="89c67-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89c67-115">Return value</span></span>

<span data-ttu-id="89c67-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="89c67-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="89c67-117">True se LHS precede o è uguale a RHS.</span><span class="sxs-lookup"><span data-stu-id="89c67-117">True if lhs comes before or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="89c67-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89c67-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="89c67-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="89c67-119">Reference</span></span>

[<span data-ttu-id="89c67-120">Struttura JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="89c67-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="89c67-121">Membri JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="89c67-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="89c67-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="89c67-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
