---
description: 'Altre informazioni su: JET_LOGTIME. Operatore di uguaglianza'
title: JET_LOGTIME. Operatore di uguaglianza
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_LOGTIME,Microsoft.Isam.Esent.Interop.JET_LOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39514101
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f346a1331200b18c2fc9e51d8eebc1ddaef105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319661"
---
# <a name="jet_logtimeequality-operator"></a><span data-ttu-id="a5f6e-103">JET_LOGTIME. Operatore di uguaglianza</span><span class="sxs-lookup"><span data-stu-id="a5f6e-103">JET_LOGTIME.Equality operator</span></span>

<span data-ttu-id="a5f6e-104">Determina se due istanze specificate di JET_LOGTIME sono uguali.</span><span class="sxs-lookup"><span data-stu-id="a5f6e-104">Determines whether two specified instances of JET_LOGTIME are equal.</span></span>

<span data-ttu-id="a5f6e-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a5f6e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a5f6e-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a5f6e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f6e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5f6e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LOGTIME, _
    rhs As JET_LOGTIME _
) As Boolean
'Usage
Dim lhs As JET_LOGTIME
Dim rhs As JET_LOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LOGTIME lhs,
    JET_LOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="a5f6e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5f6e-108">Parameters</span></span>

  - <span data-ttu-id="a5f6e-109">LHS</span><span class="sxs-lookup"><span data-stu-id="a5f6e-109">lhs</span></span>  
    <span data-ttu-id="a5f6e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="a5f6e-110">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  
    
    <span data-ttu-id="a5f6e-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="a5f6e-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="a5f6e-112">rhs</span><span class="sxs-lookup"><span data-stu-id="a5f6e-112">rhs</span></span>  
    <span data-ttu-id="a5f6e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="a5f6e-113">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  
    
    <span data-ttu-id="a5f6e-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="a5f6e-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a5f6e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5f6e-115">Return value</span></span>

<span data-ttu-id="a5f6e-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a5f6e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a5f6e-117">True se le due istanze sono uguali.</span><span class="sxs-lookup"><span data-stu-id="a5f6e-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5f6e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5f6e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a5f6e-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a5f6e-119">Reference</span></span>

[<span data-ttu-id="a5f6e-120">Struttura JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="a5f6e-120">JET_LOGTIME structure</span></span>](./jet-logtime-structure2.md)

[<span data-ttu-id="a5f6e-121">Membri JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="a5f6e-121">JET_LOGTIME members</span></span>](./jet-logtime-members.md)

[<span data-ttu-id="a5f6e-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a5f6e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
