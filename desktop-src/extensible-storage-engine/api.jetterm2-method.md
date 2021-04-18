---
description: 'Altre informazioni su: metodo API. JetTerm2'
title: API. JetTerm2, metodo
TOCTitle: 'JetTerm2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm2(v=EXCHG.10)
ms:contentKeyID: 55100829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e8a4aa8c96f9a4d0242657fe7126abf1388a7f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318823"
---
# <a name="apijetterm2-method"></a><span data-ttu-id="8a292-103">API. JetTerm2, metodo</span><span class="sxs-lookup"><span data-stu-id="8a292-103">Api.JetTerm2 method</span></span>

<span data-ttu-id="8a292-104">Terminare un'istanza di creata con [JetInit (JET_INSTANCE)](./api.jetinit-method.md) o [JetCreateInstance (JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span><span class="sxs-lookup"><span data-stu-id="8a292-104">Terminate an instance that was created with [JetInit(JET_INSTANCE)](./api.jetinit-method.md) or [JetCreateInstance(JET_INSTANCE, String)](./api.jetcreateinstance-method.md).</span></span>

<span data-ttu-id="8a292-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8a292-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8a292-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8a292-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8a292-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a292-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetTerm2 ( _
    instance As JET_INSTANCE, _
    grbit As TermGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As TermGrbitApi.JetTerm2(instance, grbit)
```

``` csharp
public static void JetTerm2(
    JET_INSTANCE instance,
    TermGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8a292-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a292-108">Parameters</span></span>

  - <span data-ttu-id="8a292-109">instance</span><span class="sxs-lookup"><span data-stu-id="8a292-109">instance</span></span>  
    <span data-ttu-id="8a292-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8a292-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="8a292-111">Istanza di da terminare.</span><span class="sxs-lookup"><span data-stu-id="8a292-111">The instance to terminate.</span></span>

<!-- end list -->

  - <span data-ttu-id="8a292-112">grbit</span><span class="sxs-lookup"><span data-stu-id="8a292-112">grbit</span></span>  
    <span data-ttu-id="8a292-113">Tipo: [Microsoft. ISAM. esent. Interop. TermGrbit](./termgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8a292-113">Type: [Microsoft.Isam.Esent.Interop.TermGrbit](./termgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8a292-114">Opzioni di terminazione.</span><span class="sxs-lookup"><span data-stu-id="8a292-114">Termination options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8a292-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a292-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8a292-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8a292-116">Reference</span></span>

[<span data-ttu-id="8a292-117">Classe API</span><span class="sxs-lookup"><span data-stu-id="8a292-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8a292-118">Membri API</span><span class="sxs-lookup"><span data-stu-id="8a292-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8a292-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8a292-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
