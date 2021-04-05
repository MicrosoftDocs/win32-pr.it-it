---
description: 'Altre informazioni su: Metodo Transaction. ReleaseResource'
title: Transaction. ReleaseResource, metodo
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Transaction.ReleaseResource
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78d3dc358b6c7c5dfe297132fd83f08c64693c85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129707"
---
# <a name="transactionreleaseresource-method"></a><span data-ttu-id="1f653-103">Transaction. ReleaseResource, metodo</span><span class="sxs-lookup"><span data-stu-id="1f653-103">Transaction.ReleaseResource method</span></span>

<span data-ttu-id="1f653-104">Chiamato quando la transazione viene eliminata quando è attiva.</span><span class="sxs-lookup"><span data-stu-id="1f653-104">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="1f653-105">Questa operazione deve eseguire il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="1f653-105">This should rollback the transaction.</span></span>

<span data-ttu-id="1f653-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f653-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1f653-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1f653-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f653-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f653-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="see-also"></a><span data-ttu-id="1f653-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="1f653-109">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f653-110">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1f653-110">Reference</span></span>

[<span data-ttu-id="1f653-111">Transaction (classe)</span><span class="sxs-lookup"><span data-stu-id="1f653-111">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="1f653-112">Membri transazione</span><span class="sxs-lookup"><span data-stu-id="1f653-112">Transaction members</span></span>](./transaction-members.md)

[<span data-ttu-id="1f653-113">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1f653-113">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
