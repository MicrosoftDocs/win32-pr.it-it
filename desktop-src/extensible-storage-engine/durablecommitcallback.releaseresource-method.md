---
description: 'Altre informazioni su: DurableCommitCallback. ReleaseResource, metodo'
title: Metodo DurableCommitCallback. ReleaseResource (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback.ReleaseResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 634dd081513e576c7aabaac17cc5f9d207a8769f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233961"
---
# <a name="durablecommitcallbackreleaseresource-method"></a><span data-ttu-id="c3e22-103">DurableCommitCallback. ReleaseResource, metodo</span><span class="sxs-lookup"><span data-stu-id="c3e22-103">DurableCommitCallback.ReleaseResource method</span></span>

<span data-ttu-id="c3e22-104">Libera la sessione di commit durevole.</span><span class="sxs-lookup"><span data-stu-id="c3e22-104">Frees the durable commit session.</span></span>

<span data-ttu-id="c3e22-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3e22-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="c3e22-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c3e22-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3e22-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3e22-107">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="remarks"></a><span data-ttu-id="c3e22-108">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="c3e22-108">Remarks</span></span>

<span data-ttu-id="c3e22-109">Non tentare di impostare il parametro di istanza su null, perché il callback viene eliminato dopo JetTerm e non è possibile impostare il callback dopo JetTerm.</span><span class="sxs-lookup"><span data-stu-id="c3e22-109">Do not try to set the instance parameter to null, because the callback is disposed after JetTerm and the callback cannot be set after JetTerm.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3e22-110">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3e22-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3e22-111">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c3e22-111">Reference</span></span>

[<span data-ttu-id="c3e22-112">Classe DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="c3e22-112">DurableCommitCallback class</span></span>](./durablecommitcallback-class.md)

[<span data-ttu-id="c3e22-113">Membri di DurableCommitCallback</span><span class="sxs-lookup"><span data-stu-id="c3e22-113">DurableCommitCallback members</span></span>](./durablecommitcallback-members.md)

[<span data-ttu-id="c3e22-114">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="c3e22-114">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
