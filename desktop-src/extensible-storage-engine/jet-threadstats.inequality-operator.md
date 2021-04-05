---
description: 'Altre informazioni su: JET_THREADSTATS. Operatore di disuguaglianza'
title: JET_THREADSTATS. Operatore di disuguaglianza (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Inequality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510396
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Inequality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9dd3bc0f56b5fbbc47928387f999664df7bcc7a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884201"
---
# <a name="jet_threadstatsinequality-operator"></a><span data-ttu-id="adb5f-103">JET_THREADSTATS. Operatore di disuguaglianza</span><span class="sxs-lookup"><span data-stu-id="adb5f-103">JET_THREADSTATS.Inequality operator</span></span>

<span data-ttu-id="adb5f-104">Determina se due istanze specificate di JET_THREADSTATS non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="adb5f-104">Determines whether two specified instances of JET_THREADSTATS are not equal.</span></span>

<span data-ttu-id="adb5f-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="adb5f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="adb5f-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="adb5f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="adb5f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="adb5f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="adb5f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="adb5f-108">Parameters</span></span>

  - <span data-ttu-id="adb5f-109">LHS</span><span class="sxs-lookup"><span data-stu-id="adb5f-109">lhs</span></span>  
    <span data-ttu-id="adb5f-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="adb5f-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="adb5f-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="adb5f-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="adb5f-112">rhs</span><span class="sxs-lookup"><span data-stu-id="adb5f-112">rhs</span></span>  
    <span data-ttu-id="adb5f-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="adb5f-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="adb5f-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="adb5f-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="adb5f-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="adb5f-115">Return value</span></span>

<span data-ttu-id="adb5f-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="adb5f-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="adb5f-117">True se le due istanze non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="adb5f-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="adb5f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="adb5f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="adb5f-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="adb5f-119">Reference</span></span>

[<span data-ttu-id="adb5f-120">Struttura JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="adb5f-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="adb5f-121">Membri JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="adb5f-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="adb5f-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="adb5f-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
