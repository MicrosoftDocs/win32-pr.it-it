---
description: 'Altre informazioni su: metodo API. JetGetCursorInfo'
title: API. JetGetCursorInfo, metodo
TOCTitle: 'JetGetCursorInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcursorinfo(v=EXCHG.10)
ms:contentKeyID: 55100707
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetCursorInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7144283a062b0097d6866e74d1c263bb130c5e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049416"
---
# <a name="apijetgetcursorinfo-method"></a><span data-ttu-id="3e48f-103">API. JetGetCursorInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="3e48f-103">Api.JetGetCursorInfo method</span></span>

<span data-ttu-id="3e48f-104">Determinare se un aggiornamento del record corrente di un cursore provocherà un conflitto di scrittura, in base allo stato corrente dell'aggiornamento del record.</span><span class="sxs-lookup"><span data-stu-id="3e48f-104">Determine whether an update of the current record of a cursor will result in a write conflict, based on the current update status of the record.</span></span> <span data-ttu-id="3e48f-105">È possibile che venga restituito un conflitto di scrittura anche se JetGetCursorInfo viene restituito correttamente.</span><span class="sxs-lookup"><span data-stu-id="3e48f-105">It is possible that a write conflict will ultimately be returned even if JetGetCursorInfo returns successfully.</span></span> <span data-ttu-id="3e48f-106">Poiché un'altra sessione può aggiornare il record prima che la sessione corrente sia in grado di aggiornare lo stesso record.</span><span class="sxs-lookup"><span data-stu-id="3e48f-106">because another session may update the record before the current session is able to update the same record.</span></span>

<span data-ttu-id="3e48f-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3e48f-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3e48f-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3e48f-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3e48f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e48f-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetCursorInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetGetCursorInfo(sesid, tableid)
```

``` csharp
public static void JetGetCursorInfo(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="3e48f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e48f-110">Parameters</span></span>

  - <span data-ttu-id="3e48f-111">sesid</span><span class="sxs-lookup"><span data-stu-id="3e48f-111">sesid</span></span>  
    <span data-ttu-id="3e48f-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3e48f-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3e48f-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="3e48f-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3e48f-114">TableID</span><span class="sxs-lookup"><span data-stu-id="3e48f-114">tableid</span></span>  
    <span data-ttu-id="3e48f-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3e48f-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3e48f-116">Cursore da verificare.</span><span class="sxs-lookup"><span data-stu-id="3e48f-116">The cursor to check.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e48f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e48f-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3e48f-118">Riferimento</span><span class="sxs-lookup"><span data-stu-id="3e48f-118">Reference</span></span>

[<span data-ttu-id="3e48f-119">Classe API</span><span class="sxs-lookup"><span data-stu-id="3e48f-119">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3e48f-120">Membri API</span><span class="sxs-lookup"><span data-stu-id="3e48f-120">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3e48f-121">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3e48f-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
