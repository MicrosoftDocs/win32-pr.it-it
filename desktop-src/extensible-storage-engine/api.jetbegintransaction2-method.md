---
description: 'Altre informazioni su: metodo API. JetBeginTransaction2'
title: API. JetBeginTransaction2, metodo
TOCTitle: 'JetBeginTransaction2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.BeginTransactionGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetbegintransaction2(v=EXCHG.10)
ms:contentKeyID: 55107226
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetBeginTransaction2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8d41652c4688bd736ac5f5164ca9b487a24edf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524770"
---
# <a name="apijetbegintransaction2-method"></a><span data-ttu-id="d7f06-103">API. JetBeginTransaction2, metodo</span><span class="sxs-lookup"><span data-stu-id="d7f06-103">Api.JetBeginTransaction2 method</span></span>

<span data-ttu-id="d7f06-104">Consente a una sessione di immettere una transazione o di creare un nuovo punto di salvataggio in una transazione esistente.</span><span class="sxs-lookup"><span data-stu-id="d7f06-104">Causes a session to enter a transaction or create a new save point in an existing transaction.</span></span>

<span data-ttu-id="d7f06-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d7f06-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d7f06-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d7f06-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f06-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7f06-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetBeginTransaction2 ( _
    sesid As JET_SESID, _
    grbit As BeginTransactionGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim grbit As BeginTransactionGrbitApi.JetBeginTransaction2(sesid, _
    grbit)
```

``` csharp
public static void JetBeginTransaction2(
    JET_SESID sesid,
    BeginTransactionGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="d7f06-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7f06-108">Parameters</span></span>

  - <span data-ttu-id="d7f06-109">sesid</span><span class="sxs-lookup"><span data-stu-id="d7f06-109">sesid</span></span>  
    <span data-ttu-id="d7f06-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="d7f06-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="d7f06-111">Sessione per la quale iniziare la transazione.</span><span class="sxs-lookup"><span data-stu-id="d7f06-111">The session to begin the transaction for.</span></span>

<!-- end list -->

  - <span data-ttu-id="d7f06-112">grbit</span><span class="sxs-lookup"><span data-stu-id="d7f06-112">grbit</span></span>  
    <span data-ttu-id="d7f06-113">Tipo: [Microsoft. ISAM. esent. Interop. BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d7f06-113">Type: [Microsoft.Isam.Esent.Interop.BeginTransactionGrbit](./begintransactiongrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="d7f06-114">Opzioni di transazione.</span><span class="sxs-lookup"><span data-stu-id="d7f06-114">Transaction options.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7f06-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7f06-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d7f06-116">Riferimento</span><span class="sxs-lookup"><span data-stu-id="d7f06-116">Reference</span></span>

[<span data-ttu-id="d7f06-117">Classe API</span><span class="sxs-lookup"><span data-stu-id="d7f06-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="d7f06-118">Membri API</span><span class="sxs-lookup"><span data-stu-id="d7f06-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="d7f06-119">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d7f06-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
