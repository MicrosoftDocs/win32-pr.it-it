---
description: 'Altre informazioni su: metodo API. JetOSSnapshotFreeze'
title: API. JetOSSnapshotFreeze, metodo
TOCTitle: 'JetOSSnapshotFreeze method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotfreeze(v=EXCHG.10)
ms:contentKeyID: 55100793
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7434cb79e90f99ab946c86a97559079352956fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233783"
---
# <a name="apijetossnapshotfreeze-method"></a><span data-ttu-id="afefc-103">API. JetOSSnapshotFreeze, metodo</span><span class="sxs-lookup"><span data-stu-id="afefc-103">Api.JetOSSnapshotFreeze method</span></span>

<span data-ttu-id="afefc-104">Avvia uno snapshot.</span><span class="sxs-lookup"><span data-stu-id="afefc-104">Starts a snapshot.</span></span> <span data-ttu-id="afefc-105">Durante l'esecuzione dello snapshot, non è possibile eseguire alcuna attività Write-to-disk da parte del motore.</span><span class="sxs-lookup"><span data-stu-id="afefc-105">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="afefc-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="afefc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="afefc-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="afefc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="afefc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afefc-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotFreeze ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotFreezeGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotFreezeGrbitApi.JetOSSnapshotFreeze(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotFreeze(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotFreezeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="afefc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="afefc-109">Parameters</span></span>

  - <span data-ttu-id="afefc-110">snapshot</span><span class="sxs-lookup"><span data-stu-id="afefc-110">snapshot</span></span>  
    <span data-ttu-id="afefc-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="afefc-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="afefc-112">Sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="afefc-112">The snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="afefc-113">numInstances</span><span class="sxs-lookup"><span data-stu-id="afefc-113">numInstances</span></span>  
    <span data-ttu-id="afefc-114">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="afefc-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="afefc-115">Restituisce il numero di istanze che fanno parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="afefc-115">Returns the number of instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="afefc-116">instances</span><span class="sxs-lookup"><span data-stu-id="afefc-116">instances</span></span>  
    <span data-ttu-id="afefc-117">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="afefc-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="afefc-118">Restituisce informazioni sulle istanze di che fanno parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="afefc-118">Returns information about the instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="afefc-119">grbit</span><span class="sxs-lookup"><span data-stu-id="afefc-119">grbit</span></span>  
    <span data-ttu-id="afefc-120">Tipo: [Microsoft. ISAM. esent. Interop. SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="afefc-120">Type: [Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="afefc-121">Opzioni di blocco dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="afefc-121">Snapshot freeze options.</span></span>

## <a name="see-also"></a><span data-ttu-id="afefc-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afefc-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="afefc-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="afefc-123">Reference</span></span>

[<span data-ttu-id="afefc-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="afefc-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="afefc-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="afefc-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="afefc-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="afefc-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
