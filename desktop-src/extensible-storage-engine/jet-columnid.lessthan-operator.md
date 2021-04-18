---
description: 'Altre informazioni su: JET_COLUMNID. Operatore LessThan'
title: JET_COLUMNID. Operatore LessThan
TOCTitle: 'LessThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_lessthan(v=EXCHG.10)
ms:contentKeyID: 39512911
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.LessThan
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_LessThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 263cb7be0377da007e6294b29701613628ec692d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305810"
---
# <a name="jet_columnidlessthan-operator"></a><span data-ttu-id="d6136-103">JET_COLUMNID. Operatore LessThan</span><span class="sxs-lookup"><span data-stu-id="d6136-103">JET_COLUMNID.LessThan operator</span></span>

<span data-ttu-id="d6136-104">Determinare se un columnid è precedente a un altro ColumnID.</span><span class="sxs-lookup"><span data-stu-id="d6136-104">Determine whether one columnid is before another columnid.</span></span>

<span data-ttu-id="d6136-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d6136-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d6136-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d6136-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d6136-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6136-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator < ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs < rhs)
```

``` csharp
public static bool operator <(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="d6136-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6136-108">Parameters</span></span>

  - <span data-ttu-id="d6136-109">LHS</span><span class="sxs-lookup"><span data-stu-id="d6136-109">lhs</span></span>  
    <span data-ttu-id="d6136-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6136-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d6136-111">Primo ColumnID da confrontare.</span><span class="sxs-lookup"><span data-stu-id="d6136-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="d6136-112">rhs</span><span class="sxs-lookup"><span data-stu-id="d6136-112">rhs</span></span>  
    <span data-ttu-id="d6136-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d6136-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="d6136-114">Secondo ColumnID da confrontare.</span><span class="sxs-lookup"><span data-stu-id="d6136-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d6136-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6136-115">Return value</span></span>

<span data-ttu-id="d6136-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="d6136-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="d6136-117">True se LHS precede RHS.</span><span class="sxs-lookup"><span data-stu-id="d6136-117">True if lhs comes before rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6136-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6136-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d6136-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d6136-119">Reference</span></span>

[<span data-ttu-id="d6136-120">Struttura JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d6136-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="d6136-121">Membri JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d6136-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="d6136-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d6136-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
