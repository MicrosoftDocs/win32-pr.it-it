---
description: 'Altre informazioni su: metodo API. JetBeginTransaction'
title: API. JetBeginTransaction, metodo
TOCTitle: 'JetBeginTransaction method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction(Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction(v=EXCHG.10)
ms:contentKeyID: 55107225
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b8812df332734ee109ea52820346e433e747751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306322"
---
# <a name="apijetbegintransaction-method"></a><span data-ttu-id="69156-103">API. JetBeginTransaction, metodo</span><span class="sxs-lookup"><span data-stu-id="69156-103">Api.JetBeginTransaction method</span></span>

<span data-ttu-id="69156-104">Consente a una sessione di immettere una transazione o di creare un nuovo punto di salvataggio in una transazione esistente.</span><span class="sxs-lookup"><span data-stu-id="69156-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="69156-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="69156-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="69156-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="69156-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="69156-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="69156-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction ( _
    sesid As JET_SESID _
)
'Usage
Dim sesid As JET_SESIDApi.JetBeginTransaction(sesid)
```

``` csharp
public static void JetBeginTransaction(
    JET_SESID sesid
)
```

#### <a name="parameters"></a><span data-ttu-id="69156-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="69156-108">Parameters</span></span>

  - <span data-ttu-id="69156-109">sesid</span><span class="sxs-lookup"><span data-stu-id="69156-109">sesid</span></span>  
    <span data-ttu-id="69156-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="69156-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="69156-111">Sessione per la quale iniziare la transazione.</span><span class="sxs-lookup"><span data-stu-id="69156-111">The session to begin the transaction for.</span></span>

## <a name="see-also"></a><span data-ttu-id="69156-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="69156-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="69156-113">Riferimento</span><span class="sxs-lookup"><span data-stu-id="69156-113">Reference</span></span>

[<span data-ttu-id="69156-114">Classe API</span><span class="sxs-lookup"><span data-stu-id="69156-114">Api class</span></span>](./api-class.md)

[<span data-ttu-id="69156-115">Membri API</span><span class="sxs-lookup"><span data-stu-id="69156-115">Api members</span></span>](./api-members.md)

[<span data-ttu-id="69156-116">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="69156-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
