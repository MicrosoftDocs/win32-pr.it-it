---
description: 'Altre informazioni su: Metodo Instance.Init (InitGrbit)'
title: Metodo Instance.Init (InitGrbit)
TOCTitle: Init method (InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103295
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3f87247a77cb89e6e5e9e20048b04f8d9fae36ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232604"
---
# <a name="instanceinit-method-initgrbit"></a><span data-ttu-id="8951a-103">Metodo Instance.Init (InitGrbit)</span><span class="sxs-lookup"><span data-stu-id="8951a-103">Instance.Init method (InitGrbit)</span></span>

<span data-ttu-id="8951a-104">Inizializzare il JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="8951a-104">Initialize the JET_INSTANCE.</span></span>

<span data-ttu-id="8951a-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8951a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8951a-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="8951a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8951a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8951a-107">Syntax</span></span>

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim grbit As InitGrbit

instance.Init(grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    InitGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8951a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8951a-108">Parameters</span></span>

  - <span data-ttu-id="8951a-109">grbit</span><span class="sxs-lookup"><span data-stu-id="8951a-109">grbit</span></span>  
    <span data-ttu-id="8951a-110">Tipo: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8951a-110">Type: [Microsoft.Isam.Esent.Interop.InitGrbit](./initgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8951a-111">Opzioni di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="8951a-111">Initialization options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8951a-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8951a-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8951a-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="8951a-113">Reference</span></span>

[<span data-ttu-id="8951a-114">Classe dell'istanza</span><span class="sxs-lookup"><span data-stu-id="8951a-114">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="8951a-115">Membri di istanza</span><span class="sxs-lookup"><span data-stu-id="8951a-115">Instance members</span></span>](./instance-members.md)

[<span data-ttu-id="8951a-116">Overload init</span><span class="sxs-lookup"><span data-stu-id="8951a-116">Init overload</span></span>](./instance.init-method2.md)

[<span data-ttu-id="8951a-117">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="8951a-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
