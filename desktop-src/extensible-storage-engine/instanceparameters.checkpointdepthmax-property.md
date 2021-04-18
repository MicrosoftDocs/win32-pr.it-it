---
description: 'Altre informazioni su: Proprietà InstanceParameters. CheckpointDepthMax'
title: Proprietà InstanceParameters. CheckpointDepthMax
TOCTitle: 'CheckpointDepthMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.checkpointdepthmax(v=EXCHG.10)
ms:contentKeyID: 55103294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3addab0356206577eda22119ddce81721e9c2bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309150"
---
# <a name="instanceparameterscheckpointdepthmax-property"></a><span data-ttu-id="0632d-103">Proprietà InstanceParameters. CheckpointDepthMax</span><span class="sxs-lookup"><span data-stu-id="0632d-103">InstanceParameters.CheckpointDepthMax property</span></span>

<span data-ttu-id="0632d-104">Ottiene o imposta la soglia in byte per informazioni sul numero di file di log delle transazioni che dovranno essere riprodotti dopo un arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="0632d-104">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="0632d-105">Se la registrazione circolare è abilitata usando CircularLog, questo parametro controllerà anche la quantità approssimativa di file di log delle transazioni che verranno conservati su disco.</span><span class="sxs-lookup"><span data-stu-id="0632d-105">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="0632d-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0632d-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0632d-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0632d-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0632d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0632d-108">Syntax</span></span>

``` vb
'Declaration
Public Property CheckpointDepthMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CheckpointDepthMax

instance.CheckpointDepthMax = value
```

``` csharp
public int CheckpointDepthMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="0632d-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="0632d-109">Property value</span></span>

<span data-ttu-id="0632d-110">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0632d-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="0632d-111">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0632d-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0632d-112">Riferimento</span><span class="sxs-lookup"><span data-stu-id="0632d-112">Reference</span></span>

[<span data-ttu-id="0632d-113">Classe InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="0632d-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="0632d-114">Membri di InstanceParameters</span><span class="sxs-lookup"><span data-stu-id="0632d-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="0632d-115">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="0632d-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
