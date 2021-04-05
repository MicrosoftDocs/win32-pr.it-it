---
description: 'Altre informazioni su: VistaApi. JetOSSnapshotEnd, metodo'
title: Metodo VistaApi. JetOSSnapshotEnd (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOSSnapshotEnd method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotend(v=EXCHG.10)
ms:contentKeyID: 55104196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 291d83929940a9f66f4e16c5088e6ec08187f908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752255"
---
# <a name="vistaapijetossnapshotend-method"></a><span data-ttu-id="e0aa6-103">VistaApi. JetOSSnapshotEnd, metodo</span><span class="sxs-lookup"><span data-stu-id="e0aa6-103">VistaApi.JetOSSnapshotEnd method</span></span>

<span data-ttu-id="e0aa6-104">Notifica al motore che la sessione snapshot è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-104">Notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="e0aa6-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e0aa6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="e0aa6-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e0aa6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e0aa6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0aa6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotEnd ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotEndGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotEndGrbitVistaApi.JetOSSnapshotEnd(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotEnd(
    JET_OSSNAPID snapshot,
    SnapshotEndGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e0aa6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0aa6-108">Parameters</span></span>

  - <span data-ttu-id="e0aa6-109">snapshot</span><span class="sxs-lookup"><span data-stu-id="e0aa6-109">snapshot</span></span>  
    <span data-ttu-id="e0aa6-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e0aa6-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="e0aa6-111">Identificatore della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-111">The identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="e0aa6-112">grbit</span><span class="sxs-lookup"><span data-stu-id="e0aa6-112">grbit</span></span>  
    <span data-ttu-id="e0aa6-113">Tipo: [Microsoft. ISAM. esent. Interop. vista. SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e0aa6-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e0aa6-114">Opzioni di fine snapshot.</span><span class="sxs-lookup"><span data-stu-id="e0aa6-114">Snapshot end options.</span></span>

## <a name="see-also"></a><span data-ttu-id="e0aa6-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e0aa6-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e0aa6-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e0aa6-116">Reference</span></span>

[<span data-ttu-id="e0aa6-117">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="e0aa6-117">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="e0aa6-118">Membri di VistaApi</span><span class="sxs-lookup"><span data-stu-id="e0aa6-118">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="e0aa6-119">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="e0aa6-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
