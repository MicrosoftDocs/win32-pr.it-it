---
description: 'Altre informazioni su: JET_BKINFO. Operatore di uguaglianza'
title: JET_BKINFO. Operatore di uguaglianza
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Equality(Microsoft.Isam.Esent.Interop.JET_BKINFO,Microsoft.Isam.Esent.Interop.JET_BKINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bkinfo.op_equality(v=EXCHG.10)
ms:contentKeyID: 39510688
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKINFO.op_Equality
- Microsoft.Isam.Esent.Interop.JET_BKINFO.Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a20cc09e55ce2bbb194561d4e371b81f9bcb2a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317403"
---
# <a name="jet_bkinfoequality-operator"></a><span data-ttu-id="8028d-103">JET_BKINFO. Operatore di uguaglianza</span><span class="sxs-lookup"><span data-stu-id="8028d-103">JET_BKINFO.Equality operator</span></span>

<span data-ttu-id="8028d-104">Determina se due istanze specificate di JET_BKINFO sono uguali.</span><span class="sxs-lookup"><span data-stu-id="8028d-104">Determines whether two specified instances of JET_BKINFO are equal.</span></span>

<span data-ttu-id="8028d-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8028d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8028d-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8028d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8028d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8028d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_BKINFO, _
    rhs As JET_BKINFO _
) As Boolean
'Usage
Dim lhs As JET_BKINFO
Dim rhs As JET_BKINFO
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_BKINFO lhs,
    JET_BKINFO rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="8028d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8028d-108">Parameters</span></span>

  - <span data-ttu-id="8028d-109">LHS</span><span class="sxs-lookup"><span data-stu-id="8028d-109">lhs</span></span>  
    <span data-ttu-id="8028d-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="8028d-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="8028d-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="8028d-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="8028d-112">rhs</span><span class="sxs-lookup"><span data-stu-id="8028d-112">rhs</span></span>  
    <span data-ttu-id="8028d-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="8028d-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKINFO](./jet-bkinfo-structure2.md)</span></span>  
    
    <span data-ttu-id="8028d-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="8028d-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8028d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8028d-115">Return value</span></span>

<span data-ttu-id="8028d-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="8028d-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="8028d-117">True se le due istanze sono uguali.</span><span class="sxs-lookup"><span data-stu-id="8028d-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8028d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8028d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8028d-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8028d-119">Reference</span></span>

[<span data-ttu-id="8028d-120">Struttura JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="8028d-120">JET_BKINFO structure</span></span>](./jet-bkinfo-structure2.md)

[<span data-ttu-id="8028d-121">Membri JET_BKINFO</span><span class="sxs-lookup"><span data-stu-id="8028d-121">JET_BKINFO members</span></span>](./jet-bkinfo-members.md)

[<span data-ttu-id="8028d-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8028d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
