---
description: 'Altre informazioni su: metodo Update. ReleaseResource'
title: Update. ReleaseResource, metodo
TOCTitle: 'ReleaseResource method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.ReleaseResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.releaseresource(v=EXCHG.10)
ms:contentKeyID: 55104200
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.ReleaseResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.ReleaseResource
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72a17022ff91f278b6a5ac4f84fc7e2d70bb04bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307796"
---
# <a name="updatereleaseresource-method"></a><span data-ttu-id="f958b-103">Update. ReleaseResource, metodo</span><span class="sxs-lookup"><span data-stu-id="f958b-103">Update.ReleaseResource method</span></span>

<span data-ttu-id="f958b-104">Chiamato quando la transazione viene eliminata quando è attiva.</span><span class="sxs-lookup"><span data-stu-id="f958b-104">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="f958b-105">Questa operazione deve eseguire il rollback della transazione.</span><span class="sxs-lookup"><span data-stu-id="f958b-105">This should rollback the transaction.</span></span>

<span data-ttu-id="f958b-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f958b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f958b-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f958b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f958b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f958b-108">Syntax</span></span>

``` vb
'Declaration
Protected Overrides Sub ReleaseResource
'Usage

Me.ReleaseResource()
```

``` csharp
protected override void ReleaseResource()
```

## <a name="see-also"></a><span data-ttu-id="f958b-109">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="f958b-109">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f958b-110">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f958b-110">Reference</span></span>

[<span data-ttu-id="f958b-111">Classe Update</span><span class="sxs-lookup"><span data-stu-id="f958b-111">Update class</span></span>](./update-class.md)

[<span data-ttu-id="f958b-112">Aggiornare i membri</span><span class="sxs-lookup"><span data-stu-id="f958b-112">Update members</span></span>](./update-members.md)

[<span data-ttu-id="f958b-113">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f958b-113">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
