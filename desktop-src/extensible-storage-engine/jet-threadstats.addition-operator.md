---
description: 'Altre informazioni su: JET_THREADSTATS. Operatore di addizione'
title: JET_THREADSTATS. Operatore di addizione (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_addition(v=EXCHG.10)
ms:contentKeyID: 39516195
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 829bf96b3c7095b95644db220a5d18c7e987e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319643"
---
# <a name="jet_threadstatsaddition-operator"></a><span data-ttu-id="c3d1d-103">JET_THREADSTATS. Operatore di addizione</span><span class="sxs-lookup"><span data-stu-id="c3d1d-103">JET_THREADSTATS.Addition operator</span></span>

<span data-ttu-id="c3d1d-104">Aggiungere le statistiche in due strutture di JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-104">Add the stats in two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="c3d1d-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3d1d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="c3d1d-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3d1d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3d1d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3d1d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 + t2)
```

``` csharp
public static JET_THREADSTATS operator +(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="c3d1d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3d1d-108">Parameters</span></span>

  - <span data-ttu-id="c3d1d-109">t1</span><span class="sxs-lookup"><span data-stu-id="c3d1d-109">t1</span></span>  
    <span data-ttu-id="c3d1d-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c3d1d-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="c3d1d-111">Primo JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3d1d-112">T2</span><span class="sxs-lookup"><span data-stu-id="c3d1d-112">t2</span></span>  
    <span data-ttu-id="c3d1d-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c3d1d-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="c3d1d-114">Secondo JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c3d1d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3d1d-115">Return value</span></span>

<span data-ttu-id="c3d1d-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c3d1d-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="c3d1d-117">JET_THREADSTATS contenente il risultato dell'aggiunta delle statistiche in T1 e T2.</span><span class="sxs-lookup"><span data-stu-id="c3d1d-117">A JET_THREADSTATS containing the result of adding the stats in t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c3d1d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3d1d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3d1d-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c3d1d-119">Reference</span></span>

[<span data-ttu-id="c3d1d-120">Struttura JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="c3d1d-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="c3d1d-121">Membri JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="c3d1d-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="c3d1d-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="c3d1d-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
