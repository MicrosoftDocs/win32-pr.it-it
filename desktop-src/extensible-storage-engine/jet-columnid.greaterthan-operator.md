---
description: 'Altre informazioni su: JET_COLUMNID. GreaterThan (operatore)'
title: JET_COLUMNID. GreaterThan (operatore)
TOCTitle: 'GreaterThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThan(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_greaterthan(v=EXCHG.10)
ms:contentKeyID: 39513070
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThan
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThan
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 16105651443aad050a1bbaf4a9dee1e68a5042fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318146"
---
# <a name="jet_columnidgreaterthan-operator"></a><span data-ttu-id="9e940-103">JET_COLUMNID. GreaterThan (operatore)</span><span class="sxs-lookup"><span data-stu-id="9e940-103">JET_COLUMNID.GreaterThan operator</span></span>

<span data-ttu-id="9e940-104">Determinare se un columnid è successivo a un altro ColumnID.</span><span class="sxs-lookup"><span data-stu-id="9e940-104">Determine whether one columnid is after another columnid.</span></span>

<span data-ttu-id="9e940-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9e940-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9e940-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9e940-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9e940-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e940-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator > ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs > rhs)
```

``` csharp
public static bool operator >(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="9e940-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e940-108">Parameters</span></span>

  - <span data-ttu-id="9e940-109">LHS</span><span class="sxs-lookup"><span data-stu-id="9e940-109">lhs</span></span>  
    <span data-ttu-id="9e940-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9e940-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="9e940-111">Primo ColumnID da confrontare.</span><span class="sxs-lookup"><span data-stu-id="9e940-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="9e940-112">rhs</span><span class="sxs-lookup"><span data-stu-id="9e940-112">rhs</span></span>  
    <span data-ttu-id="9e940-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9e940-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="9e940-114">Secondo ColumnID da confrontare.</span><span class="sxs-lookup"><span data-stu-id="9e940-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9e940-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e940-115">Return value</span></span>

<span data-ttu-id="9e940-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="9e940-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="9e940-117">True se LHS viene eseguito dopo RHS.</span><span class="sxs-lookup"><span data-stu-id="9e940-117">True if lhs comes after rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9e940-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e940-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9e940-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9e940-119">Reference</span></span>

[<span data-ttu-id="9e940-120">Struttura JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9e940-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="9e940-121">Membri JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="9e940-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="9e940-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9e940-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
