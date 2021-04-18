---
description: 'Altre informazioni su: metodo API. JetSetSessionContext'
title: API. JetSetSessionContext, metodo
TOCTitle: 'JetSetSessionContext method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext(Microsoft.Isam.Esent.Interop.JET_SESID,System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsessioncontext(v=EXCHG.10)
ms:contentKeyID: 55100820
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSessionContext
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d73a382a2b8e176e2d1ce6fa13585a6b5fa103e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316963"
---
# <a name="apijetsetsessioncontext-method"></a><span data-ttu-id="24366-103">API. JetSetSessionContext, metodo</span><span class="sxs-lookup"><span data-stu-id="24366-103">Api.JetSetSessionContext method</span></span>

<span data-ttu-id="24366-104">Associa una sessione al thread corrente usando l'handle di contesto specificato.</span><span class="sxs-lookup"><span data-stu-id="24366-104">Associates a session with the current thread using the given context handle.</span></span> <span data-ttu-id="24366-105">Questa associazione esegue l'override del requisito del motore predefinito che una transazione per una determinata sessione deve essere interamente eseguita sullo stesso thread.</span><span class="sxs-lookup"><span data-stu-id="24366-105">This association overrides the default engine requirement that a transaction for a given session must occur entirely on the same thread.</span></span> <span data-ttu-id="24366-106">Utilizzare [JetResetSessionContext (JET_SESID)](./api.jetresetsessioncontext-method.md) per rimuovere l'associazione.</span><span class="sxs-lookup"><span data-stu-id="24366-106">Use [JetResetSessionContext(JET_SESID)](./api.jetresetsessioncontext-method.md) to remove the association.</span></span>

<span data-ttu-id="24366-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="24366-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="24366-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="24366-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="24366-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="24366-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionContext ( _
    sesid As JET_SESID, _
    context As IntPtr _
)
'Usage
Dim sesid As JET_SESID
Dim context As IntPtrApi.JetSetSessionContext(sesid, _
    context)
```

``` csharp
public static void JetSetSessionContext(
    JET_SESID sesid,
    IntPtr context
)
```

#### <a name="parameters"></a><span data-ttu-id="24366-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="24366-110">Parameters</span></span>

  - <span data-ttu-id="24366-111">sesid</span><span class="sxs-lookup"><span data-stu-id="24366-111">sesid</span></span>  
    <span data-ttu-id="24366-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="24366-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="24366-113">Sessione in cui impostare il contesto.</span><span class="sxs-lookup"><span data-stu-id="24366-113">The session to set the context on.</span></span>

<!-- end list -->

  - <span data-ttu-id="24366-114">contesto</span><span class="sxs-lookup"><span data-stu-id="24366-114">context</span></span>  
    <span data-ttu-id="24366-115">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="24366-115">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="24366-116">Contesto da impostare.</span><span class="sxs-lookup"><span data-stu-id="24366-116">The context to set.</span></span>

## <a name="see-also"></a><span data-ttu-id="24366-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="24366-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="24366-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="24366-118">Reference</span></span>

[<span data-ttu-id="24366-119">Classe API</span><span class="sxs-lookup"><span data-stu-id="24366-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="24366-120">Membri API</span><span class="sxs-lookup"><span data-stu-id="24366-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="24366-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="24366-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
