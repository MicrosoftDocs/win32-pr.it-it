---
description: 'Altre informazioni su: VistaApi. JetOSSnapshotTruncateLogInstance, metodo'
title: Metodo VistaApi. JetOSSnapshotTruncateLogInstance (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75d694629585a730f5c1c7b9b08bb7b06e735cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885773"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a><span data-ttu-id="052ab-103">VistaApi. JetOSSnapshotTruncateLogInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="052ab-103">VistaApi.JetOSSnapshotTruncateLogInstance method</span></span>

<span data-ttu-id="052ab-104">Tronca il log per un'istanza specificata durante una sessione snapshot.</span><span class="sxs-lookup"><span data-stu-id="052ab-104">Truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="052ab-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="052ab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="052ab-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="052ab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="052ab-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="052ab-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="052ab-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="052ab-108">Parameters</span></span>

  - <span data-ttu-id="052ab-109">snapshot</span><span class="sxs-lookup"><span data-stu-id="052ab-109">snapshot</span></span>  
    <span data-ttu-id="052ab-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="052ab-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="052ab-111">Identificatore dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="052ab-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="052ab-112">instance</span><span class="sxs-lookup"><span data-stu-id="052ab-112">instance</span></span>  
    <span data-ttu-id="052ab-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="052ab-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="052ab-114">Istanza per la quale troncare il log.</span><span class="sxs-lookup"><span data-stu-id="052ab-114">The instance to truncat the log for.</span></span>

<!-- end list -->

  - <span data-ttu-id="052ab-115">grbit</span><span class="sxs-lookup"><span data-stu-id="052ab-115">grbit</span></span>  
    <span data-ttu-id="052ab-116">Tipo: [Microsoft. ISAM. esent. Interop. vista. SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="052ab-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="052ab-117">Opzioni per questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="052ab-117">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="052ab-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="052ab-118">Remarks</span></span>

<span data-ttu-id="052ab-119">Questa funzione deve essere chiamata solo se lo snapshot è stato creato con l'opzione [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) .</span><span class="sxs-lookup"><span data-stu-id="052ab-119">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="052ab-120">In caso contrario, la sessione snapshot termina dopo la chiamata a [JetOSSnapshotThaw (JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span><span class="sxs-lookup"><span data-stu-id="052ab-120">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="052ab-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="052ab-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="052ab-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="052ab-122">Reference</span></span>

[<span data-ttu-id="052ab-123">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="052ab-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="052ab-124">Membri di VistaApi</span><span class="sxs-lookup"><span data-stu-id="052ab-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="052ab-125">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="052ab-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
