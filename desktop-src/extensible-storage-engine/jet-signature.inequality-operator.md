---
description: 'Altre informazioni su: JET_SIGNATURE. Operatore di disuguaglianza'
title: JET_SIGNATURE. Operatore di disuguaglianza
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 646b97f37aea55ee3e9d1aa24e80b9d26ea82469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315642"
---
# <a name="jet_signatureinequality-operator"></a><span data-ttu-id="c3640-103">JET_SIGNATURE. Operatore di disuguaglianza</span><span class="sxs-lookup"><span data-stu-id="c3640-103">JET_SIGNATURE.Inequality operator</span></span>

<span data-ttu-id="c3640-104">Determina se due istanze specificate di JET_SIGNATURE non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="c3640-104">Determines whether two specified instances of JET_SIGNATURE are not equal.</span></span>

<span data-ttu-id="c3640-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3640-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3640-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3640-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3640-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3640-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="c3640-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3640-108">Parameters</span></span>

  - <span data-ttu-id="c3640-109">LHS</span><span class="sxs-lookup"><span data-stu-id="c3640-109">lhs</span></span>  
    <span data-ttu-id="c3640-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c3640-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="c3640-111">Prima istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="c3640-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3640-112">rhs</span><span class="sxs-lookup"><span data-stu-id="c3640-112">rhs</span></span>  
    <span data-ttu-id="c3640-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c3640-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="c3640-114">Seconda istanza da confrontare.</span><span class="sxs-lookup"><span data-stu-id="c3640-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c3640-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3640-115">Return value</span></span>

<span data-ttu-id="c3640-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="c3640-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="c3640-117">True se le due istanze non sono uguali.</span><span class="sxs-lookup"><span data-stu-id="c3640-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3640-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3640-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3640-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c3640-119">Reference</span></span>

[<span data-ttu-id="c3640-120">Struttura JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="c3640-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="c3640-121">Membri JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="c3640-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="c3640-122">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c3640-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
