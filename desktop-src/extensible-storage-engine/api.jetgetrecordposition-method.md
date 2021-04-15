---
description: 'Altre informazioni su: metodo API. JetGetRecordPosition'
title: API. JetGetRecordPosition, metodo
TOCTitle: 'JetGetRecordPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetrecordposition(v=EXCHG.10)
ms:contentKeyID: 55100722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetRecordPosition
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 00350853172d784c270c197e7c58ad6fa616560f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525608"
---
# <a name="apijetgetrecordposition-method"></a><span data-ttu-id="4f55c-103">API. JetGetRecordPosition, metodo</span><span class="sxs-lookup"><span data-stu-id="4f55c-103">Api.JetGetRecordPosition method</span></span>

<span data-ttu-id="4f55c-104">Restituisce la posizione frazionaria del record corrente nell'indice corrente sotto forma di struttura [JET_RECPOS](./jet-recpos-class.md) .</span><span class="sxs-lookup"><span data-stu-id="4f55c-104">Returns the fractional position of the current record in the current index in the form of a [JET_RECPOS](./jet-recpos-class.md) structure.</span></span> <span data-ttu-id="4f55c-105">Vedere anche [JetGotoPosition (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span><span class="sxs-lookup"><span data-stu-id="4f55c-105">Also see [JetGotoPosition(JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgotoposition-method.md).</span></span>

<span data-ttu-id="4f55c-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4f55c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4f55c-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4f55c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4f55c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4f55c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGetRecordPosition(sesid, _
    tableid, recpos)
```

``` csharp
public static void JetGetRecordPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_RECPOS recpos
)
```

#### <a name="parameters"></a><span data-ttu-id="4f55c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4f55c-109">Parameters</span></span>

  - <span data-ttu-id="4f55c-110">sesid</span><span class="sxs-lookup"><span data-stu-id="4f55c-110">sesid</span></span>  
    <span data-ttu-id="4f55c-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4f55c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4f55c-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="4f55c-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f55c-113">TableID</span><span class="sxs-lookup"><span data-stu-id="4f55c-113">tableid</span></span>  
    <span data-ttu-id="4f55c-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4f55c-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4f55c-115">Cursore posizionato sul record.</span><span class="sxs-lookup"><span data-stu-id="4f55c-115">The cursor positioned on the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="4f55c-116">recpos</span><span class="sxs-lookup"><span data-stu-id="4f55c-116">recpos</span></span>  
    <span data-ttu-id="4f55c-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span><span class="sxs-lookup"><span data-stu-id="4f55c-117">Type: [Microsoft.Isam.Esent.Interop.JET_RECPOS](./jet-recpos-class.md)</span></span>  
    
    <span data-ttu-id="4f55c-118">Restituisce la posizione frazionaria approssimativa del record.</span><span class="sxs-lookup"><span data-stu-id="4f55c-118">Returns the approximate fractional position of the record.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f55c-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4f55c-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4f55c-120">Riferimento</span><span class="sxs-lookup"><span data-stu-id="4f55c-120">Reference</span></span>

[<span data-ttu-id="4f55c-121">Classe API</span><span class="sxs-lookup"><span data-stu-id="4f55c-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4f55c-122">Membri API</span><span class="sxs-lookup"><span data-stu-id="4f55c-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4f55c-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="4f55c-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
