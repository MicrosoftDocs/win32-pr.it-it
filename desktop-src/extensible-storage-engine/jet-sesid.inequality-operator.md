---
description: 'Altre informazioni su: JET_SESID. Operatore di disuguaglianza'
title: JET_SESID. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39514305
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e42b5e21937ae8af4ccd04708520ece40558c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128658"
---
# <a name="jet_sesidinequality-operator"></a><span data-ttu-id="e0bf1-103">JET_SESID. Operatore di disuguaglianza</span><span class="sxs-lookup"><span data-stu-id="e0bf1-103">JET_SESID.Inequality operator</span></span>

<span data-ttu-id="e0bf1-104">Determina se due istanze specificate di JET_SESID non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="e0bf1-104">Determines whether two specified instances of JET_SESID are not equal.</span></span>

<span data-ttu-id="e0bf1-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e0bf1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e0bf1-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e0bf1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e0bf1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0bf1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="e0bf1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0bf1-108">Parameters</span></span>

  - <span data-ttu-id="e0bf1-109">LHS</span><span class="sxs-lookup"><span data-stu-id="e0bf1-109">lhs</span></span>  
    <span data-ttu-id="e0bf1-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e0bf1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e0bf1-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="e0bf1-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="e0bf1-112">rhs</span><span class="sxs-lookup"><span data-stu-id="e0bf1-112">rhs</span></span>  
    <span data-ttu-id="e0bf1-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e0bf1-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e0bf1-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="e0bf1-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e0bf1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0bf1-115">Return value</span></span>

<span data-ttu-id="e0bf1-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e0bf1-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e0bf1-117">True se le due istanze non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="e0bf1-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e0bf1-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0bf1-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e0bf1-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e0bf1-119">Reference</span></span>

[<span data-ttu-id="e0bf1-120">Struttura JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e0bf1-120">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="e0bf1-121">Membri JET_SESID</span><span class="sxs-lookup"><span data-stu-id="e0bf1-121">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="e0bf1-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="e0bf1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
