---
description: 'Altre informazioni su: Proprietà EsentStopwatch. ThreadStats'
title: Proprietà EsentStopwatch. ThreadStats
TOCTitle: 'ThreadStats property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentstopwatch.threadstats(v=EXCHG.10)
ms:contentKeyID: 55102996
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentStopwatch.get_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.set_ThreadStats
- Microsoft.Isam.Esent.Interop.EsentStopwatch.ThreadStats
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 241b7d80e86eb3c773aecd58b7d16e749e040611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313593"
---
# <a name="esentstopwatchthreadstats-property"></a><span data-ttu-id="9d86d-103">Proprietà EsentStopwatch. ThreadStats</span><span class="sxs-lookup"><span data-stu-id="9d86d-103">EsentStopwatch.ThreadStats property</span></span>

<span data-ttu-id="9d86d-104">Ottiene le statistiche di lavoro ESENT totali misurate dall'istanza corrente.</span><span class="sxs-lookup"><span data-stu-id="9d86d-104">Gets the total ESENT work stats measured by the current instance.</span></span>

<span data-ttu-id="9d86d-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9d86d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9d86d-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9d86d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9d86d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9d86d-107">Syntax</span></span>

``` vb
'Declaration
Public Property ThreadStats As JET_THREADSTATS
    Get
    Private Set
'Usage
Dim instance As EsentStopwatch
Dim value As JET_THREADSTATS

value = instance.ThreadStats
```

``` csharp
public JET_THREADSTATS ThreadStats { get; private set; }
```

#### <a name="property-value"></a><span data-ttu-id="9d86d-108">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="9d86d-108">Property value</span></span>

<span data-ttu-id="9d86d-109">Tipo: [Microsoft.ISAM.esent.Interop.vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9d86d-109">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="9d86d-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9d86d-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9d86d-111">Riferimento</span><span class="sxs-lookup"><span data-stu-id="9d86d-111">Reference</span></span>

[<span data-ttu-id="9d86d-112">Classe EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="9d86d-112">EsentStopwatch class</span></span>](./esentstopwatch-class.md)

[<span data-ttu-id="9d86d-113">Membri di EsentStopwatch</span><span class="sxs-lookup"><span data-stu-id="9d86d-113">EsentStopwatch members</span></span>](./esentstopwatch-members.md)

[<span data-ttu-id="9d86d-114">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="9d86d-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
