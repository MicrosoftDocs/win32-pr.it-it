---
description: 'Altre informazioni su: JET_THREADSTATS. Metodo Subtract'
title: JET_THREADSTATS. Metodo Subtract (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.subtract(v=EXCHG.10)
ms:contentKeyID: 39514465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf1f47258fe965c41b0a02ccbb32712b0a54c97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316461"
---
# <a name="jet_threadstatssubtract-method"></a><span data-ttu-id="d45d3-103">JET_THREADSTATS. Metodo Subtract</span><span class="sxs-lookup"><span data-stu-id="d45d3-103">JET_THREADSTATS.Subtract method</span></span>

<span data-ttu-id="d45d3-104">Calcolare la differenza nelle statistiche tra due strutture di JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="d45d3-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="d45d3-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d45d3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d45d3-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d45d3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d45d3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d45d3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Subtract(t1, t2)
```

``` csharp
public static JET_THREADSTATS Subtract(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="d45d3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d45d3-108">Parameters</span></span>

  - <span data-ttu-id="d45d3-109">t1</span><span class="sxs-lookup"><span data-stu-id="d45d3-109">t1</span></span>  
    <span data-ttu-id="d45d3-110">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d45d3-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="d45d3-111">Primo JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="d45d3-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="d45d3-112">T2</span><span class="sxs-lookup"><span data-stu-id="d45d3-112">t2</span></span>  
    <span data-ttu-id="d45d3-113">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d45d3-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="d45d3-114">Secondo JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="d45d3-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d45d3-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d45d3-115">Return value</span></span>

<span data-ttu-id="d45d3-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d45d3-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="d45d3-117">JET_THREADSTATS contenente la differenza nelle statistiche tra T1 e T2.</span><span class="sxs-lookup"><span data-stu-id="d45d3-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d45d3-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d45d3-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d45d3-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d45d3-119">Reference</span></span>

[<span data-ttu-id="d45d3-120">Struttura JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="d45d3-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="d45d3-121">Membri JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="d45d3-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="d45d3-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="d45d3-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
