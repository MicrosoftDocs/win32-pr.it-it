---
description: 'Altre informazioni su: JET_COLUMNID. Operatore di uguaglianza'
title: JET_COLUMNID. Operatore di uguaglianza
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Equality(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39514850
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equality
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79d6d376d9a574587e5e3fc5329a7c092da73a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348841"
---
# <a name="jet_columnidequality-operator"></a><span data-ttu-id="8fb15-103">JET_COLUMNID. Operatore di uguaglianza</span><span class="sxs-lookup"><span data-stu-id="8fb15-103">JET_COLUMNID.Equality operator</span></span>

<span data-ttu-id="8fb15-104">Determina se due istanze specificate di JET_COLUMNID sono uguali.</span><span class="sxs-lookup"><span data-stu-id="8fb15-104">Determines whether two specified instances of JET_COLUMNID are equal.</span></span>

<span data-ttu-id="8fb15-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8fb15-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8fb15-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8fb15-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb15-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fb15-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="8fb15-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fb15-108">Parameters</span></span>

  - <span data-ttu-id="8fb15-109">LHS</span><span class="sxs-lookup"><span data-stu-id="8fb15-109">lhs</span></span>  
    <span data-ttu-id="8fb15-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8fb15-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="8fb15-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="8fb15-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="8fb15-112">rhs</span><span class="sxs-lookup"><span data-stu-id="8fb15-112">rhs</span></span>  
    <span data-ttu-id="8fb15-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8fb15-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="8fb15-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="8fb15-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="8fb15-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fb15-115">Return value</span></span>

<span data-ttu-id="8fb15-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="8fb15-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="8fb15-117">True se le due istanze sono uguali.</span><span class="sxs-lookup"><span data-stu-id="8fb15-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8fb15-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fb15-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8fb15-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8fb15-119">Reference</span></span>

[<span data-ttu-id="8fb15-120">Struttura JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="8fb15-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="8fb15-121">Membri JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="8fb15-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="8fb15-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8fb15-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
