---
description: 'Altre informazioni su: JET_THREADSTATS. Metodo Create'
title: JET_THREADSTATS. Metodo Create (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'Create method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create(System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.create(v=EXCHG.10)
ms:contentKeyID: 39509886
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Create
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: beaaee85fc0f6c331db1d813280d4b900e39fb54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758492"
---
# <a name="jet_threadstatscreate-method"></a><span data-ttu-id="4bedb-103">JET_THREADSTATS. Metodo Create</span><span class="sxs-lookup"><span data-stu-id="4bedb-103">JET_THREADSTATS.Create method</span></span>

<span data-ttu-id="4bedb-104">Crea una nuova struttura di [JET_THREADSTATS](./jet-threadstats-structure2.md) con il valore specificato.</span><span class="sxs-lookup"><span data-stu-id="4bedb-104">Create a new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified valued.</span></span>

<span data-ttu-id="4bedb-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4bedb-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="4bedb-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4bedb-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4bedb-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4bedb-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Create ( _
    cPageReferenced As Integer, _
    cPageRead As Integer, _
    cPagePreread As Integer, _
    cPageDirtied As Integer, _
    cPageRedirtied As Integer, _
    cLogRecord As Integer, _
    cbLogRecord As Integer _
) As JET_THREADSTATS
'Usage
Dim cPageReferenced As Integer
Dim cPageRead As Integer
Dim cPagePreread As Integer
Dim cPageDirtied As Integer
Dim cPageRedirtied As Integer
Dim cLogRecord As Integer
Dim cbLogRecord As Integer
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Create(cPageReferenced, _
    cPageRead, cPagePreread, cPageDirtied, _
    cPageRedirtied, cLogRecord, cbLogRecord)
```

``` csharp
public static JET_THREADSTATS Create(
    int cPageReferenced,
    int cPageRead,
    int cPagePreread,
    int cPageDirtied,
    int cPageRedirtied,
    int cLogRecord,
    int cbLogRecord
)
```

#### <a name="parameters"></a><span data-ttu-id="4bedb-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4bedb-108">Parameters</span></span>

  - <span data-ttu-id="4bedb-109">cPageReferenced</span><span class="sxs-lookup"><span data-stu-id="4bedb-109">cPageReferenced</span></span>  
    <span data-ttu-id="4bedb-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4bedb-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4bedb-111">Numero di pagine visitate.</span><span class="sxs-lookup"><span data-stu-id="4bedb-111">Number of pages visited.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bedb-112">cPageRead</span><span class="sxs-lookup"><span data-stu-id="4bedb-112">cPageRead</span></span>  
    <span data-ttu-id="4bedb-113">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4bedb-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4bedb-114">Numero di pagine lette.</span><span class="sxs-lookup"><span data-stu-id="4bedb-114">Number of pages read.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bedb-115">cPagePreread</span><span class="sxs-lookup"><span data-stu-id="4bedb-115">cPagePreread</span></span>  
    <span data-ttu-id="4bedb-116">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4bedb-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4bedb-117">Numero di pagine prelette.</span><span class="sxs-lookup"><span data-stu-id="4bedb-117">Number of pages preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bedb-118">cPageDirtied</span><span class="sxs-lookup"><span data-stu-id="4bedb-118">cPageDirtied</span></span>  
    <span data-ttu-id="4bedb-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4bedb-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4bedb-120">TNumber delle pagine sporche.</span><span class="sxs-lookup"><span data-stu-id="4bedb-120">TNumber of pages dirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bedb-121">cPageRedirtied</span><span class="sxs-lookup"><span data-stu-id="4bedb-121">cPageRedirtied</span></span>  
    <span data-ttu-id="4bedb-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4bedb-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4bedb-123">Numero di pagine risporche.</span><span class="sxs-lookup"><span data-stu-id="4bedb-123">Number of pages redirtied.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bedb-124">cLogRecord</span><span class="sxs-lookup"><span data-stu-id="4bedb-124">cLogRecord</span></span>  
    <span data-ttu-id="4bedb-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4bedb-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4bedb-126">Numero di record di log generati.</span><span class="sxs-lookup"><span data-stu-id="4bedb-126">Number of log records generated.</span></span>

<!-- end list -->

  - <span data-ttu-id="4bedb-127">cbLogRecord</span><span class="sxs-lookup"><span data-stu-id="4bedb-127">cbLogRecord</span></span>  
    <span data-ttu-id="4bedb-128">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4bedb-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4bedb-129">Byte dei record di log scritti.</span><span class="sxs-lookup"><span data-stu-id="4bedb-129">Bytes of log records written.</span></span>

#### <a name="return-value"></a><span data-ttu-id="4bedb-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4bedb-130">Return value</span></span>

<span data-ttu-id="4bedb-131">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4bedb-131">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="4bedb-132">Nuovo [JET_THREADSTATS](./jet-threadstats-structure2.md) struct con i valori specificati.</span><span class="sxs-lookup"><span data-stu-id="4bedb-132">A new [JET_THREADSTATS](./jet-threadstats-structure2.md) struct with the specified values.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4bedb-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4bedb-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4bedb-134">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4bedb-134">Reference</span></span>

[<span data-ttu-id="4bedb-135">Struttura JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="4bedb-135">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="4bedb-136">Membri JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="4bedb-136">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="4bedb-137">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="4bedb-137">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
