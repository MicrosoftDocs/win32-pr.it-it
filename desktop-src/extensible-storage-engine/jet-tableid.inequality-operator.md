---
description: 'Altre informazioni su: JET_TABLEID. Operatore di disuguaglianza'
title: JET_TABLEID. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510333
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Inequality
- Microsoft.Isam.Esent.Interop.JET_TABLEID.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7e1cfc9a43beb8478be287e1659883d49f62239
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529298"
---
# <a name="jet_tableidinequality-operator"></a><span data-ttu-id="b4b0e-103">JET_TABLEID. Operatore di disuguaglianza</span><span class="sxs-lookup"><span data-stu-id="b4b0e-103">JET_TABLEID.Inequality operator</span></span>

<span data-ttu-id="b4b0e-104">Determina se due istanze specificate di JET_TABLEID non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-104">Determines whether two specified instances of JET_TABLEID are not equal.</span></span>

<span data-ttu-id="b4b0e-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b4b0e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b4b0e-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b4b0e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b0e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b4b0e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_TABLEID, _
    rhs As JET_TABLEID _
) As Boolean
'Usage
Dim lhs As JET_TABLEID
Dim rhs As JET_TABLEID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_TABLEID lhs,
    JET_TABLEID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b4b0e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4b0e-108">Parameters</span></span>

  - <span data-ttu-id="b4b0e-109">LHS</span><span class="sxs-lookup"><span data-stu-id="b4b0e-109">lhs</span></span>  
    <span data-ttu-id="b4b0e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b4b0e-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b4b0e-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b4b0e-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b4b0e-112">rhs</span></span>  
    <span data-ttu-id="b4b0e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b4b0e-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b4b0e-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b4b0e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4b0e-115">Return value</span></span>

<span data-ttu-id="b4b0e-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b4b0e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b4b0e-117">True se le due istanze non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="b4b0e-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b4b0e-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4b0e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4b0e-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b4b0e-119">Reference</span></span>

[<span data-ttu-id="b4b0e-120">Struttura JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b4b0e-120">JET_TABLEID structure</span></span>](./jet-tableid-structure.md)

[<span data-ttu-id="b4b0e-121">Membri JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="b4b0e-121">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="b4b0e-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b4b0e-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
