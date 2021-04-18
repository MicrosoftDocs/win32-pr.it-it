---
description: 'Altre informazioni su: operatore JET_COMMIT_ID. disuguaglianza'
title: Operatore JET_COMMIT_ID. disuguaglianza (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Inequality(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_inequality(v=EXCHG.10)
ms:contentKeyID: 55104411
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_Inequality
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b64be3b2c6438490d3e44076b1e553a7abb37d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315150"
---
# <a name="jet_commit_idinequality-operator"></a><span data-ttu-id="2b6ac-103">Operatore JET_COMMIT_ID. disuguaglianza</span><span class="sxs-lookup"><span data-stu-id="2b6ac-103">JET_COMMIT_ID.Inequality operator</span></span>

<span data-ttu-id="2b6ac-104">Determinare se un commitid non è uguale a un altro commitid.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-104">Determine whether one commitid is not equal to another commitid.</span></span>

<span data-ttu-id="2b6ac-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2b6ac-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="2b6ac-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2b6ac-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6ac-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b6ac-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="2b6ac-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b6ac-108">Parameters</span></span>

  - <span data-ttu-id="2b6ac-109">LHS</span><span class="sxs-lookup"><span data-stu-id="2b6ac-109">lhs</span></span>  
    <span data-ttu-id="2b6ac-110">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="2b6ac-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="2b6ac-111">Primo oggetto commitid da confrontare.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="2b6ac-112">rhs</span><span class="sxs-lookup"><span data-stu-id="2b6ac-112">rhs</span></span>  
    <span data-ttu-id="2b6ac-113">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="2b6ac-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="2b6ac-114">Secondo oggetto commitid da confrontare.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="2b6ac-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b6ac-115">Return value</span></span>

<span data-ttu-id="2b6ac-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="2b6ac-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="2b6ac-117">True se LHS viene visualizzato non è uguale a RHS.</span><span class="sxs-lookup"><span data-stu-id="2b6ac-117">True if lhs comes is not equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2b6ac-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b6ac-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2b6ac-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="2b6ac-119">Reference</span></span>

[<span data-ttu-id="2b6ac-120">Classe JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="2b6ac-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="2b6ac-121">Membri JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="2b6ac-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="2b6ac-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="2b6ac-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
