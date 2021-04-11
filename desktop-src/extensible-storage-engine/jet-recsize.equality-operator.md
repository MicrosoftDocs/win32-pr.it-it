---
description: 'Altre informazioni su: JET_RECSIZE. Operatore di uguaglianza'
title: JET_RECSIZE. Operatore di uguaglianza (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515439
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f95ee6975a71e40d702b1f68c47ad6831881ffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128199"
---
# <a name="jet_recsizeequality-operator"></a><span data-ttu-id="40e0b-103">JET_RECSIZE. Operatore di uguaglianza</span><span class="sxs-lookup"><span data-stu-id="40e0b-103">JET_RECSIZE.Equality operator</span></span>

<span data-ttu-id="40e0b-104">Determina se due istanze specificate di JET_RECSIZE sono uguali.</span><span class="sxs-lookup"><span data-stu-id="40e0b-104">Determines whether two specified instances of JET_RECSIZE are equal.</span></span>

<span data-ttu-id="40e0b-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40e0b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="40e0b-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="40e0b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40e0b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40e0b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_RECSIZE, _
    rhs As JET_RECSIZE _
) As Boolean
'Usage
Dim lhs As JET_RECSIZE
Dim rhs As JET_RECSIZE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_RECSIZE lhs,
    JET_RECSIZE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="40e0b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="40e0b-108">Parameters</span></span>

  - <span data-ttu-id="40e0b-109">LHS</span><span class="sxs-lookup"><span data-stu-id="40e0b-109">lhs</span></span>  
    <span data-ttu-id="40e0b-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="40e0b-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="40e0b-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="40e0b-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="40e0b-112">rhs</span><span class="sxs-lookup"><span data-stu-id="40e0b-112">rhs</span></span>  
    <span data-ttu-id="40e0b-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="40e0b-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="40e0b-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="40e0b-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="40e0b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40e0b-115">Return value</span></span>

<span data-ttu-id="40e0b-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="40e0b-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="40e0b-117">True se le due istanze sono uguali.</span><span class="sxs-lookup"><span data-stu-id="40e0b-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="40e0b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40e0b-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40e0b-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="40e0b-119">Reference</span></span>

[<span data-ttu-id="40e0b-120">Struttura JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="40e0b-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="40e0b-121">Membri JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="40e0b-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="40e0b-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="40e0b-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
