---
description: 'Altre informazioni su: metodo API. JetTruncateLogInstance'
title: API. JetTruncateLogInstance, metodo
TOCTitle: 'JetTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jettruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55100815
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc1693b3f84cd594bfeca81a8e854e49e28d955f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968540"
---
# <a name="apijettruncateloginstance-method"></a><span data-ttu-id="cf116-103">API. JetTruncateLogInstance, metodo</span><span class="sxs-lookup"><span data-stu-id="cf116-103">Api.JetTruncateLogInstance method</span></span>

<span data-ttu-id="cf116-104">Utilizzato durante un backup avviato da JetBeginExternalBackup per eliminare tutti i file di log delle transazioni che non saranno più necessari dopo il completamento corretto del backup corrente.</span><span class="sxs-lookup"><span data-stu-id="cf116-104">Used during a backup initiated by JetBeginExternalBackup to delete any transaction log files that will no longer be needed once the current backup completes successfully.</span></span>

<span data-ttu-id="cf116-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cf116-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cf116-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cf116-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cf116-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cf116-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTruncateLogInstance ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTruncateLogInstance(instance)
```

``` csharp
public static void JetTruncateLogInstance(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a><span data-ttu-id="cf116-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cf116-108">Parameters</span></span>

  - <span data-ttu-id="cf116-109">instance</span><span class="sxs-lookup"><span data-stu-id="cf116-109">instance</span></span>  
    <span data-ttu-id="cf116-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="cf116-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="cf116-111">Istanza da troncare.</span><span class="sxs-lookup"><span data-stu-id="cf116-111">The instance to truncate.</span></span>

## <a name="see-also"></a><span data-ttu-id="cf116-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cf116-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cf116-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="cf116-113">Reference</span></span>

[<span data-ttu-id="cf116-114">Classe API</span><span class="sxs-lookup"><span data-stu-id="cf116-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="cf116-115">Membri API</span><span class="sxs-lookup"><span data-stu-id="cf116-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="cf116-116">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="cf116-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
