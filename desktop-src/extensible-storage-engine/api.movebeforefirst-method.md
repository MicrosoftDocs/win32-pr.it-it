---
description: 'Altre informazioni su: metodo API. MoveBeforeFirst'
title: API. MoveBeforeFirst, metodo
TOCTitle: 'MoveBeforeFirst method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MoveBeforeFirst(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.movebeforefirst(v=EXCHG.10)
ms:contentKeyID: 55100849
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.MoveBeforeFirst
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.MoveBeforeFirst
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c3e49762c0d2be1f416181f5c07fb06b088d161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305560"
---
# <a name="apimovebeforefirst-method"></a><span data-ttu-id="c5e3a-103">API. MoveBeforeFirst, metodo</span><span class="sxs-lookup"><span data-stu-id="c5e3a-103">Api.MoveBeforeFirst method</span></span>

<span data-ttu-id="c5e3a-104">Posizionare il cursore prima del primo record nella tabella.</span><span class="sxs-lookup"><span data-stu-id="c5e3a-104">Position the cursor before the first record in the table.</span></span> <span data-ttu-id="c5e3a-105">Uno spostamento successivo posiziona il cursore sul primo record.</span><span class="sxs-lookup"><span data-stu-id="c5e3a-105">A subsequent move next will position the cursor on the first record.</span></span>

<span data-ttu-id="c5e3a-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c5e3a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c5e3a-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c5e3a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e3a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5e3a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MoveBeforeFirst ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.MoveBeforeFirst(sesid, tableid)
```

``` csharp
public static void MoveBeforeFirst(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="c5e3a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5e3a-109">Parameters</span></span>

  - <span data-ttu-id="c5e3a-110">sesid</span><span class="sxs-lookup"><span data-stu-id="c5e3a-110">sesid</span></span>  
    <span data-ttu-id="c5e3a-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c5e3a-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c5e3a-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c5e3a-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c5e3a-113">TableID</span><span class="sxs-lookup"><span data-stu-id="c5e3a-113">tableid</span></span>  
    <span data-ttu-id="c5e3a-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c5e3a-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c5e3a-115">Tabella da posizionare.</span><span class="sxs-lookup"><span data-stu-id="c5e3a-115">The table to position.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5e3a-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5e3a-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5e3a-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c5e3a-117">Reference</span></span>

[<span data-ttu-id="c5e3a-118">Classe API</span><span class="sxs-lookup"><span data-stu-id="c5e3a-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c5e3a-119">Membri API</span><span class="sxs-lookup"><span data-stu-id="c5e3a-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c5e3a-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c5e3a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
