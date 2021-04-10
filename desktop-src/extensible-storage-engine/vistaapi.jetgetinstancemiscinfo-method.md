---
description: 'Altre informazioni su: VistaApi. JetGetInstanceMiscInfo, metodo'
title: Metodo VistaApi. JetGetInstanceMiscInfo (Microsoft. ISAM. esent. Interop. vista)
TOCTitle: 'JetGetInstanceMiscInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE@,Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetinstancemiscinfo(v=EXCHG.10)
ms:contentKeyID: 55104187
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetInstanceMiscInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 204beee343a717d5b45d8003e123bbbe186437d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880337"
---
# <a name="vistaapijetgetinstancemiscinfo-method"></a><span data-ttu-id="d19f9-103">VistaApi. JetGetInstanceMiscInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="d19f9-103">VistaApi.JetGetInstanceMiscInfo method</span></span>

<span data-ttu-id="d19f9-104">Recupera le informazioni su un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="d19f9-104">Retrieves information about an instance.</span></span>

<span data-ttu-id="d19f9-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d19f9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d19f9-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d19f9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d19f9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d19f9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetInstanceMiscInfo ( _
    instance As JET_INSTANCE, _
    <OutAttribute> ByRef signature As JET_SIGNATURE, _
    infoLevel As JET_InstanceMiscInfo _
)
'Usage
Dim instance As JET_INSTANCE
Dim signature As JET_SIGNATURE
Dim infoLevel As JET_InstanceMiscInfoVistaApi.JetGetInstanceMiscInfo(instance, _
    signature, infoLevel)
```

``` csharp
public static void JetGetInstanceMiscInfo(
    JET_INSTANCE instance,
    out JET_SIGNATURE signature,
    JET_InstanceMiscInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="d19f9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d19f9-108">Parameters</span></span>

  - <span data-ttu-id="d19f9-109">instance</span><span class="sxs-lookup"><span data-stu-id="d19f9-109">instance</span></span>  
    <span data-ttu-id="d19f9-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d19f9-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="d19f9-111">Istanza di per cui ottenere informazioni.</span><span class="sxs-lookup"><span data-stu-id="d19f9-111">The instance to get information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="d19f9-112">firma</span><span class="sxs-lookup"><span data-stu-id="d19f9-112">signature</span></span>  
    <span data-ttu-id="d19f9-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="d19f9-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="d19f9-114">Informazioni recuperate.</span><span class="sxs-lookup"><span data-stu-id="d19f9-114">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="d19f9-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="d19f9-115">infoLevel</span></span>  
    <span data-ttu-id="d19f9-116">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d19f9-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_InstanceMiscInfo](./jet-instancemiscinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="d19f9-117">Tipo di informazioni da recuperare.</span><span class="sxs-lookup"><span data-stu-id="d19f9-117">The type of information to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="d19f9-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d19f9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d19f9-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d19f9-119">Reference</span></span>

[<span data-ttu-id="d19f9-120">Classe VistaApi</span><span class="sxs-lookup"><span data-stu-id="d19f9-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="d19f9-121">Membri di VistaApi</span><span class="sxs-lookup"><span data-stu-id="d19f9-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="d19f9-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. vista</span><span class="sxs-lookup"><span data-stu-id="d19f9-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
