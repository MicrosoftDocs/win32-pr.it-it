---
description: 'Altre informazioni su: JET_LGPOS. Operatore di disuguaglianza'
title: JET_LGPOS. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Inequality(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511705
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_LGPOS.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e324131591f1d6bee3c00e6260f31f6580ec086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968050"
---
# <a name="jet_lgposinequality-operator"></a><span data-ttu-id="b53b8-103">JET_LGPOS. Operatore di disuguaglianza</span><span class="sxs-lookup"><span data-stu-id="b53b8-103">JET_LGPOS.Inequality operator</span></span>

<span data-ttu-id="b53b8-104">Determina se due istanze specificate di JET_LGPOS non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="b53b8-104">Determines whether two specified instances of JET_LGPOS are not equal.</span></span>

<span data-ttu-id="b53b8-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b53b8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b53b8-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b53b8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b53b8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b53b8-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b53b8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b53b8-108">Parameters</span></span>

  - <span data-ttu-id="b53b8-109">LHS</span><span class="sxs-lookup"><span data-stu-id="b53b8-109">lhs</span></span>  
    <span data-ttu-id="b53b8-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b53b8-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="b53b8-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b53b8-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b53b8-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b53b8-112">rhs</span></span>  
    <span data-ttu-id="b53b8-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b53b8-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="b53b8-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b53b8-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b53b8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b53b8-115">Return value</span></span>

<span data-ttu-id="b53b8-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b53b8-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b53b8-117">True se le due istanze non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="b53b8-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b53b8-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b53b8-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b53b8-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b53b8-119">Reference</span></span>

[<span data-ttu-id="b53b8-120">Struttura JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="b53b8-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="b53b8-121">Membri JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="b53b8-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="b53b8-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b53b8-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
