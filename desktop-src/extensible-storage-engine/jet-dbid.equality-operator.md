---
description: 'Altre informazioni su: JET_DBID. Operatore di uguaglianza'
title: JET_DBID. Operatore di uguaglianza
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.op_Equality(Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equality
- Microsoft.Isam.Esent.Interop.JET_DBID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f9e99de78665d07e1e5a800f5520a39eb05e74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527445"
---
# <a name="jet_dbidequality-operator"></a><span data-ttu-id="6c096-103">JET_DBID. Operatore di uguaglianza</span><span class="sxs-lookup"><span data-stu-id="6c096-103">JET_DBID.Equality operator</span></span>

<span data-ttu-id="6c096-104">Determina se due istanze specificate di JET_DBID sono uguali.</span><span class="sxs-lookup"><span data-stu-id="6c096-104">Determines whether two specified instances of JET_DBID are equal.</span></span>

<span data-ttu-id="6c096-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6c096-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6c096-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6c096-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6c096-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c096-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_DBID, _
    rhs As JET_DBID _
) As Boolean
'Usage
Dim lhs As JET_DBID
Dim rhs As JET_DBID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_DBID lhs,
    JET_DBID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="6c096-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c096-108">Parameters</span></span>

  - <span data-ttu-id="6c096-109">LHS</span><span class="sxs-lookup"><span data-stu-id="6c096-109">lhs</span></span>  
    <span data-ttu-id="6c096-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c096-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="6c096-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="6c096-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="6c096-112">rhs</span><span class="sxs-lookup"><span data-stu-id="6c096-112">rhs</span></span>  
    <span data-ttu-id="6c096-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6c096-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="6c096-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="6c096-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6c096-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c096-115">Return value</span></span>

<span data-ttu-id="6c096-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="6c096-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="6c096-117">True se le due istanze sono uguali.</span><span class="sxs-lookup"><span data-stu-id="6c096-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6c096-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c096-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6c096-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6c096-119">Reference</span></span>

[<span data-ttu-id="6c096-120">Struttura JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6c096-120">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="6c096-121">Membri JET_DBID</span><span class="sxs-lookup"><span data-stu-id="6c096-121">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="6c096-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6c096-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
