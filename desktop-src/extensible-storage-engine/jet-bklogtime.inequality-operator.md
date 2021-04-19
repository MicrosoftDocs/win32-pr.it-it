---
description: 'Altre informazioni su: JET_BKLOGTIME. Operatore di disuguaglianza'
title: JET_BKLOGTIME. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512908
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42f13a1068543caaa590015151b523c1a441c806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317401"
---
# <a name="jet_bklogtimeinequality-operator"></a><span data-ttu-id="4055a-103">JET_BKLOGTIME. Operatore di disuguaglianza</span><span class="sxs-lookup"><span data-stu-id="4055a-103">JET_BKLOGTIME.Inequality operator</span></span>

<span data-ttu-id="4055a-104">Determina se due istanze specificate di JET_BKLOGTIME non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="4055a-104">Determines whether two specified instances of JET_BKLOGTIME are not equal.</span></span>

<span data-ttu-id="4055a-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4055a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4055a-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4055a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4055a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4055a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="4055a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4055a-108">Parameters</span></span>

  - <span data-ttu-id="4055a-109">LHS</span><span class="sxs-lookup"><span data-stu-id="4055a-109">lhs</span></span>  
    <span data-ttu-id="4055a-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4055a-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="4055a-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="4055a-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="4055a-112">rhs</span><span class="sxs-lookup"><span data-stu-id="4055a-112">rhs</span></span>  
    <span data-ttu-id="4055a-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4055a-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="4055a-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="4055a-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4055a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4055a-115">Return value</span></span>

<span data-ttu-id="4055a-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="4055a-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="4055a-117">True se le due istanze non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="4055a-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4055a-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4055a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4055a-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4055a-119">Reference</span></span>

[<span data-ttu-id="4055a-120">Struttura JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="4055a-120">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="4055a-121">Membri JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="4055a-121">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="4055a-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4055a-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
