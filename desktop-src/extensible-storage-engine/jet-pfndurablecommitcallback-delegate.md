---
description: 'Altre informazioni su: JET_PFNDURABLECOMMITCALLBACK delegate'
title: Delegato JET_PFNDURABLECOMMITCALLBACK (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: JET_PFNDURABLECOMMITCALLBACK delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_pfndurablecommitcallback(v=EXCHG.10)
ms:contentKeyID: 55104327
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.Invoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.EndInvoke
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK..ctor
- Microsoft.Isam.Esent.Interop.Windows8.JET_PFNDURABLECOMMITCALLBACK.BeginInvoke
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d9ff2f613138103be56db3fe7084202965a949cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885590"
---
# <a name="jet_pfndurablecommitcallback-delegate"></a><span data-ttu-id="d726d-103">Delegato JET_PFNDURABLECOMMITCALLBACK</span><span class="sxs-lookup"><span data-stu-id="d726d-103">JET_PFNDURABLECOMMITCALLBACK delegate</span></span>

<span data-ttu-id="d726d-104">Callback per JET_paramDurableCommitCallback.</span><span class="sxs-lookup"><span data-stu-id="d726d-104">Callback for JET_paramDurableCommitCallback.</span></span>

<span data-ttu-id="d726d-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d726d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="d726d-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d726d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d726d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d726d-107">Syntax</span></span>

``` vb
'Declaration
Public Delegate Function JET_PFNDURABLECOMMITCALLBACK ( _
    instance As JET_INSTANCE, _
    pCommitIdSeen As JET_COMMIT_ID, _
    grbit As DurableCommitCallbackGrbit _
) As JET_err
'Usage
Dim instance As New JET_PFNDURABLECOMMITCALLBACK(AddressOf HandlerMethod)
```

``` csharp
public delegate JET_err JET_PFNDURABLECOMMITCALLBACK(
    JET_INSTANCE instance,
    JET_COMMIT_ID pCommitIdSeen,
    DurableCommitCallbackGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d726d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d726d-108">Parameters</span></span>

  - <span data-ttu-id="d726d-109">instance</span><span class="sxs-lookup"><span data-stu-id="d726d-109">instance</span></span>  
    <span data-ttu-id="d726d-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d726d-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="d726d-111">Istanza da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="d726d-111">Instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="d726d-112">pCommitIdSeen</span><span class="sxs-lookup"><span data-stu-id="d726d-112">pCommitIdSeen</span></span>  
    <span data-ttu-id="d726d-113">Tipo: [Microsoft.ISAM.esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="d726d-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="d726d-114">Commit-ID appena scaricato.</span><span class="sxs-lookup"><span data-stu-id="d726d-114">Commit-id that has just been flushed.</span></span>

<!-- end list -->

  - <span data-ttu-id="d726d-115">grbit</span><span class="sxs-lookup"><span data-stu-id="d726d-115">grbit</span></span>  
    <span data-ttu-id="d726d-116">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d726d-116">Type: [Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallbackGrbit](./durablecommitcallbackgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d726d-117">Attualmente riservata.</span><span class="sxs-lookup"><span data-stu-id="d726d-117">Reserved currently.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d726d-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d726d-118">Return value</span></span>

<span data-ttu-id="d726d-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d726d-119">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="d726d-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d726d-120">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d726d-121">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d726d-121">Reference</span></span>

[<span data-ttu-id="d726d-122">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="d726d-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
