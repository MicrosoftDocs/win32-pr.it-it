---
description: 'Altre informazioni su: JET_BKLOGTIME. Operatore di uguaglianza'
title: JET_BKLOGTIME. Operatore di uguaglianza
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515956
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f5a75a1fc55159fc5ea71dba09dc1ed54194b940
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319686"
---
# <a name="jet_bklogtimeequality-operator"></a><span data-ttu-id="b1028-103">JET_BKLOGTIME. Operatore di uguaglianza</span><span class="sxs-lookup"><span data-stu-id="b1028-103">JET_BKLOGTIME.Equality operator</span></span>

<span data-ttu-id="b1028-104">Determina se due istanze specificate di JET_BKLOGTIME sono uguali.</span><span class="sxs-lookup"><span data-stu-id="b1028-104">Determines whether two specified instances of JET_BKLOGTIME are equal.</span></span>

<span data-ttu-id="b1028-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b1028-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b1028-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b1028-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b1028-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1028-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b1028-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1028-108">Parameters</span></span>

  - <span data-ttu-id="b1028-109">LHS</span><span class="sxs-lookup"><span data-stu-id="b1028-109">lhs</span></span>  
    <span data-ttu-id="b1028-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b1028-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="b1028-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b1028-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b1028-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b1028-112">rhs</span></span>  
    <span data-ttu-id="b1028-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="b1028-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="b1028-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b1028-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b1028-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1028-115">Return value</span></span>

<span data-ttu-id="b1028-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b1028-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b1028-117">True se le due istanze sono uguali.</span><span class="sxs-lookup"><span data-stu-id="b1028-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b1028-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1028-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1028-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b1028-119">Reference</span></span>

[<span data-ttu-id="b1028-120">Struttura JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="b1028-120">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="b1028-121">Membri JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="b1028-121">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="b1028-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b1028-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
