---
description: 'Altre informazioni su: JET_OSSNAPID. Operatore di disuguaglianza'
title: JET_OSSNAPID. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_OSSNAPID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ossnapid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510705
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.Inequality
- Microsoft.Isam.Esent.Interop.JET_OSSNAPID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4bb19425b9f4ce9a3d404c5b5019adf1b3a84d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760214"
---
# <a name="jet_ossnapidinequality-operator"></a><span data-ttu-id="a19d2-103">JET_OSSNAPID. Operatore di disuguaglianza</span><span class="sxs-lookup"><span data-stu-id="a19d2-103">JET_OSSNAPID.Inequality operator</span></span>

<span data-ttu-id="a19d2-104">Determina se due istanze specificate di JET_OSSNAPID non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="a19d2-104">Determines whether two specified instances of JET_OSSNAPID are not equal.</span></span>

<span data-ttu-id="a19d2-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a19d2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a19d2-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a19d2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a19d2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a19d2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_OSSNAPID, _
    rhs As JET_OSSNAPID _
) As Boolean
'Usage
Dim lhs As JET_OSSNAPID
Dim rhs As JET_OSSNAPID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_OSSNAPID lhs,
    JET_OSSNAPID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="a19d2-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a19d2-108">Parameters</span></span>

  - <span data-ttu-id="a19d2-109">LHS</span><span class="sxs-lookup"><span data-stu-id="a19d2-109">lhs</span></span>  
    <span data-ttu-id="a19d2-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a19d2-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="a19d2-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="a19d2-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="a19d2-112">rhs</span><span class="sxs-lookup"><span data-stu-id="a19d2-112">rhs</span></span>  
    <span data-ttu-id="a19d2-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a19d2-113">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="a19d2-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="a19d2-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a19d2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a19d2-115">Return value</span></span>

<span data-ttu-id="a19d2-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a19d2-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a19d2-117">True se le due istanze non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="a19d2-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a19d2-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a19d2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a19d2-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a19d2-119">Reference</span></span>

[<span data-ttu-id="a19d2-120">Struttura JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="a19d2-120">JET_OSSNAPID structure</span></span>](./jet-ossnapid-structure.md)

[<span data-ttu-id="a19d2-121">Membri JET_OSSNAPID</span><span class="sxs-lookup"><span data-stu-id="a19d2-121">JET_OSSNAPID members</span></span>](./jet-ossnapid-members.md)

[<span data-ttu-id="a19d2-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a19d2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
