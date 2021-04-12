---
description: 'Altre informazioni su: JET_INSTANCE. Operatore di disuguaglianza'
title: JET_INSTANCE. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d537b01d3485e7f5e2d1d629c005a228eac92306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132054"
---
# <a name="jet_instanceinequality-operator"></a><span data-ttu-id="e1aa4-103">JET_INSTANCE. Operatore di disuguaglianza</span><span class="sxs-lookup"><span data-stu-id="e1aa4-103">JET_INSTANCE.Inequality operator</span></span>

<span data-ttu-id="e1aa4-104">Determina se due istanze specificate di JET_INSTANCE non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="e1aa4-104">Determines whether two specified instances of JET_INSTANCE are not equal.</span></span>

<span data-ttu-id="e1aa4-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e1aa4-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e1aa4-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e1aa4-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e1aa4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1aa4-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="e1aa4-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1aa4-108">Parameters</span></span>

  - <span data-ttu-id="e1aa4-109">LHS</span><span class="sxs-lookup"><span data-stu-id="e1aa4-109">lhs</span></span>  
    <span data-ttu-id="e1aa4-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e1aa4-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="e1aa4-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="e1aa4-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="e1aa4-112">rhs</span><span class="sxs-lookup"><span data-stu-id="e1aa4-112">rhs</span></span>  
    <span data-ttu-id="e1aa4-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e1aa4-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="e1aa4-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="e1aa4-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e1aa4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1aa4-115">Return value</span></span>

<span data-ttu-id="e1aa4-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e1aa4-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e1aa4-117">True se le due istanze non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="e1aa4-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e1aa4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1aa4-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e1aa4-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e1aa4-119">Reference</span></span>

[<span data-ttu-id="e1aa4-120">Struttura JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e1aa4-120">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="e1aa4-121">Membri JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="e1aa4-121">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="e1aa4-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e1aa4-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
