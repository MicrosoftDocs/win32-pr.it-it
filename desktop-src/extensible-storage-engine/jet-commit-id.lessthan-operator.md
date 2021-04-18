---
description: 'Altre informazioni su: JET_COMMIT_ID. LessThan (operatore)'
title: Operatore JET_COMMIT_ID. LessThan (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'LessThan operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThan(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_lessthan(v=EXCHG.10)
ms:contentKeyID: 55104300
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThan
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.LessThan
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_LessThan
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: faf5363d8e53d14eb022404f7ab39fe1c7850928
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308501"
---
# <a name="jet_commit_idlessthan-operator"></a><span data-ttu-id="399d0-103">Operatore JET_COMMIT_ID. LessThan</span><span class="sxs-lookup"><span data-stu-id="399d0-103">JET_COMMIT_ID.LessThan operator</span></span>

<span data-ttu-id="399d0-104">Determinare se un commitid è precedente a un altro commitid.</span><span class="sxs-lookup"><span data-stu-id="399d0-104">Determine whether one commitid is before another commitid.</span></span>

<span data-ttu-id="399d0-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="399d0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="399d0-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="399d0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="399d0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="399d0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator < ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs < rhs)
```

``` csharp
public static bool operator <(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="399d0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="399d0-108">Parameters</span></span>

  - <span data-ttu-id="399d0-109">LHS</span><span class="sxs-lookup"><span data-stu-id="399d0-109">lhs</span></span>  
    <span data-ttu-id="399d0-110">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="399d0-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="399d0-111">Primo oggetto commitid da confrontare.</span><span class="sxs-lookup"><span data-stu-id="399d0-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="399d0-112">rhs</span><span class="sxs-lookup"><span data-stu-id="399d0-112">rhs</span></span>  
    <span data-ttu-id="399d0-113">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="399d0-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="399d0-114">Secondo oggetto commitid da confrontare.</span><span class="sxs-lookup"><span data-stu-id="399d0-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="399d0-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="399d0-115">Return value</span></span>

<span data-ttu-id="399d0-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="399d0-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="399d0-117">True se LHS precede RHS.</span><span class="sxs-lookup"><span data-stu-id="399d0-117">True if lhs comes before rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="399d0-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="399d0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="399d0-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="399d0-119">Reference</span></span>

[<span data-ttu-id="399d0-120">Classe JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="399d0-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="399d0-121">Membri JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="399d0-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="399d0-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="399d0-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
