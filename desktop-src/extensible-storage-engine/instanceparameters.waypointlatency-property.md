---
description: 'Altre informazioni su: Proprietà InstanceParameters. WaypointLatency'
title: Proprietà InstanceParameters. WaypointLatency
TOCTitle: 'WaypointLatency property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55103325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_WaypointLatency
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d7d837d7fff804926529ec67780e319d85031f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319212"
---
# <a name="instanceparameterswaypointlatency-property"></a><span data-ttu-id="6e7c3-103">Proprietà InstanceParameters. WaypointLatency</span><span class="sxs-lookup"><span data-stu-id="6e7c3-103">InstanceParameters.WaypointLatency property</span></span>

<span data-ttu-id="6e7c3-104">Ottiene o imposta il numero di registri per i quali ESENT rinvia gli scaricamenti del database.</span><span class="sxs-lookup"><span data-stu-id="6e7c3-104">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="6e7c3-105">Questa operazione può essere utilizzata per aumentare la recuperabilità del database se gli errori determinano la perdita di file di registro.</span><span class="sxs-lookup"><span data-stu-id="6e7c3-105">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="6e7c3-106">Supportato su Windows 7 e su.</span><span class="sxs-lookup"><span data-stu-id="6e7c3-106">Supported on Windows 7 and up.</span></span> <span data-ttu-id="6e7c3-107">Ignorato in Windows XP, Windows Server 2003, Windows Vista e Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6e7c3-107">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="6e7c3-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6e7c3-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6e7c3-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6e7c3-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6e7c3-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e7c3-110">Syntax</span></span>

``` vb
'Declaration
Public Property WaypointLatency As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.WaypointLatency

instance.WaypointLatency = value
```

``` csharp
public int WaypointLatency { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="6e7c3-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6e7c3-111">Property value</span></span>

<span data-ttu-id="6e7c3-112">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6e7c3-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="6e7c3-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e7c3-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e7c3-114">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6e7c3-114">Reference</span></span>

[<span data-ttu-id="6e7c3-115">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="6e7c3-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="6e7c3-116">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="6e7c3-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="6e7c3-117">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6e7c3-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
