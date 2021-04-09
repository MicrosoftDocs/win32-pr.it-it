---
description: 'Altre informazioni su: metodo API. JetDelete'
title: API. JetDelete, metodo
TOCTitle: 'JetDelete method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetDelete(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetdelete(v=EXCHG.10)
ms:contentKeyID: 55100681
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetDelete
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbc3decf125b8d3f3f1df7228852901cca90aae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878886"
---
# <a name="apijetdelete-method"></a><span data-ttu-id="81d9f-103">API. JetDelete, metodo</span><span class="sxs-lookup"><span data-stu-id="81d9f-103">Api.JetDelete method</span></span>

<span data-ttu-id="81d9f-104">Elimina il record corrente in una tabella di database.</span><span class="sxs-lookup"><span data-stu-id="81d9f-104">Deletes the current record in a database table.</span></span>

<span data-ttu-id="81d9f-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="81d9f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="81d9f-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="81d9f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="81d9f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="81d9f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetDelete ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetDelete(sesid, tableid)
```

``` csharp
public static void JetDelete(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="81d9f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="81d9f-108">Parameters</span></span>

  - <span data-ttu-id="81d9f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="81d9f-109">sesid</span></span>  
    <span data-ttu-id="81d9f-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="81d9f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="81d9f-111">Sessione che ha aperto il cursore.</span><span class="sxs-lookup"><span data-stu-id="81d9f-111">The session that opened the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="81d9f-112">TableID</span><span class="sxs-lookup"><span data-stu-id="81d9f-112">tableid</span></span>  
    <span data-ttu-id="81d9f-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="81d9f-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="81d9f-114">Cursore su una tabella di database.</span><span class="sxs-lookup"><span data-stu-id="81d9f-114">The cursor on a database table.</span></span> <span data-ttu-id="81d9f-115">La riga corrente verrà eliminata.</span><span class="sxs-lookup"><span data-stu-id="81d9f-115">The current row will be deleted.</span></span>

## <a name="see-also"></a><span data-ttu-id="81d9f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81d9f-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="81d9f-117">Riferimento</span><span class="sxs-lookup"><span data-stu-id="81d9f-117">Reference</span></span>

[<span data-ttu-id="81d9f-118">Classe API</span><span class="sxs-lookup"><span data-stu-id="81d9f-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="81d9f-119">Membri API</span><span class="sxs-lookup"><span data-stu-id="81d9f-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="81d9f-120">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="81d9f-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
