---
description: 'Altre informazioni su: Server2003Api. JetOSSnapshotAbort, metodo'
title: Metodo Server2003Api. JetOSSnapshotAbort (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: 'JetOSSnapshotAbort method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetossnapshotabort(v=EXCHG.10)
ms:contentKeyID: 55104209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44ee61a7c6cff7fe90a77fdaced786532457c132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308492"
---
# <a name="server2003apijetossnapshotabort-method"></a><span data-ttu-id="d0965-103">Server2003Api. JetOSSnapshotAbort, metodo</span><span class="sxs-lookup"><span data-stu-id="d0965-103">Server2003Api.JetOSSnapshotAbort method</span></span>

<span data-ttu-id="d0965-104">Notifica al motore che è possibile riprendere le normali operazioni di i/o dopo un periodo di blocco terminato con uno snapshot non riuscito.</span><span class="sxs-lookup"><span data-stu-id="d0965-104">Notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="d0965-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d0965-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="d0965-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d0965-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0965-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0965-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotAbort ( _
    snapid As JET_OSSNAPID, _
    grbit As SnapshotAbortGrbit _
)
'Usage
Dim snapid As JET_OSSNAPID
Dim grbit As SnapshotAbortGrbitServer2003Api.JetOSSnapshotAbort(snapid, _
    grbit)
```

``` csharp
public static void JetOSSnapshotAbort(
    JET_OSSNAPID snapid,
    SnapshotAbortGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d0965-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0965-108">Parameters</span></span>

  - <span data-ttu-id="d0965-109">snapid</span><span class="sxs-lookup"><span data-stu-id="d0965-109">snapid</span></span>  
    <span data-ttu-id="d0965-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d0965-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="d0965-111">Identificatore della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="d0965-111">Identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="d0965-112">grbit</span><span class="sxs-lookup"><span data-stu-id="d0965-112">grbit</span></span>  
    <span data-ttu-id="d0965-113">Tipo: [Microsoft. ISAM. esent. Interop. Server2003. SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d0965-113">Type: [Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d0965-114">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="d0965-114">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="d0965-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0965-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0965-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d0965-116">Reference</span></span>

[<span data-ttu-id="d0965-117">Classe Server2003Api</span><span class="sxs-lookup"><span data-stu-id="d0965-117">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="d0965-118">Membri di Server2003Api</span><span class="sxs-lookup"><span data-stu-id="d0965-118">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="d0965-119">Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="d0965-119">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
