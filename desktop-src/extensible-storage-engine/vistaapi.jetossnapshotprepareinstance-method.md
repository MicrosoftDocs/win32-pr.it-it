---
description: 'Altre informazioni su: VistaApi. JetOSSnapshotPrepareInstance, metodo'
title: Metodo VistaApi. JetOSSnapshotPrepareInstance (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOSSnapshotPrepareInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotprepareinstance(v=EXCHG.10)
ms:contentKeyID: 55104304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46151e2b11c669ac9635ce5974757999a8636b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131755"
---
# <a name="vistaapijetossnapshotprepareinstance-method"></a><span data-ttu-id="aca90-103">VistaApi. JetOSSnapshotPrepareInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="aca90-103">VistaApi.JetOSSnapshotPrepareInstance method</span></span>

<span data-ttu-id="aca90-104">Consente di selezionare un'istanza specifica che deve far parte della sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="aca90-104">Selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="aca90-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="aca90-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="aca90-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="aca90-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="aca90-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aca90-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepareInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotPrepareInstanceGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotPrepareInstanceGrbitVistaApi.JetOSSnapshotPrepareInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotPrepareInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotPrepareInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="aca90-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="aca90-108">Parameters</span></span>

  - <span data-ttu-id="aca90-109">snapshot</span><span class="sxs-lookup"><span data-stu-id="aca90-109">snapshot</span></span>  
    <span data-ttu-id="aca90-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aca90-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="aca90-111">Identificatore dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="aca90-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="aca90-112">instance</span><span class="sxs-lookup"><span data-stu-id="aca90-112">instance</span></span>  
    <span data-ttu-id="aca90-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="aca90-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="aca90-114">Istanza di da aggiungere allo snapshot.</span><span class="sxs-lookup"><span data-stu-id="aca90-114">The instance to add to the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="aca90-115">grbit</span><span class="sxs-lookup"><span data-stu-id="aca90-115">grbit</span></span>  
    <span data-ttu-id="aca90-116">Tipo: [Microsoft. ISAM. esent. Interop. vista. SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="aca90-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="aca90-117">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="aca90-117">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="aca90-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aca90-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="aca90-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="aca90-119">Reference</span></span>

[<span data-ttu-id="aca90-120">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="aca90-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="aca90-121">Membri di VistaApi</span><span class="sxs-lookup"><span data-stu-id="aca90-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="aca90-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="aca90-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
