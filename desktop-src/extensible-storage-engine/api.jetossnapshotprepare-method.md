---
description: 'Altre informazioni su: metodo API. JetOSSnapshotPrepare'
title: API. JetOSSnapshotPrepare, metodo
TOCTitle: 'JetOSSnapshotPrepare method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare(Microsoft.Isam.Esent.Interop.JET_OSSNAPID@,Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotprepare(v=EXCHG.10)
ms:contentKeyID: 55100779
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ac304cf522e7c99a2495925da8571b2139c0a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233782"
---
# <a name="apijetossnapshotprepare-method"></a><span data-ttu-id="f9f61-103">API. JetOSSnapshotPrepare, metodo</span><span class="sxs-lookup"><span data-stu-id="f9f61-103">Api.JetOSSnapshotPrepare method</span></span>

<span data-ttu-id="f9f61-104">Inizia le preparazioni per una sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="f9f61-104">Begins the preparations for a snapshot session.</span></span> <span data-ttu-id="f9f61-105">Una sessione snapshot è un breve intervallo di tempo in cui il motore non rilascia alcun disco IOs su disco, in modo che il motore possa partecipare a una sessione di snapshot del volume (se basata su uno snapshot writer).</span><span class="sxs-lookup"><span data-stu-id="f9f61-105">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="f9f61-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f9f61-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f9f61-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f9f61-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f9f61-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9f61-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepare ( _
    <OutAttribute> ByRef snapshot As JET_OSSNAPID, _
    grbit As SnapshotPrepareGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotPrepareGrbitApi.JetOSSnapshotPrepare(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotPrepare(
    out JET_OSSNAPID snapshot,
    SnapshotPrepareGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f9f61-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9f61-109">Parameters</span></span>

  - <span data-ttu-id="f9f61-110">snapshot</span><span class="sxs-lookup"><span data-stu-id="f9f61-110">snapshot</span></span>  
    <span data-ttu-id="f9f61-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f9f61-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="f9f61-112">Restituisce l'ID della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="f9f61-112">Returns the ID of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="f9f61-113">grbit</span><span class="sxs-lookup"><span data-stu-id="f9f61-113">grbit</span></span>  
    <span data-ttu-id="f9f61-114">Tipo: [Microsoft. ISAM. esent. Interop. SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f9f61-114">Type: [Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f9f61-115">Opzioni snapshot.</span><span class="sxs-lookup"><span data-stu-id="f9f61-115">Snapshot options.</span></span>

## <a name="see-also"></a><span data-ttu-id="f9f61-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9f61-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f9f61-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f9f61-117">Reference</span></span>

[<span data-ttu-id="f9f61-118">Classe API</span><span class="sxs-lookup"><span data-stu-id="f9f61-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f9f61-119">Membri API</span><span class="sxs-lookup"><span data-stu-id="f9f61-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f9f61-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f9f61-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
