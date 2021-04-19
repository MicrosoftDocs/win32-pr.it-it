---
description: 'Altre informazioni su: Windows8Api. JetSetCursorFilter, metodo'
title: Metodo Windows8Api. JetSetCursorFilter (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetSetCursorFilter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_COLUMN[],Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetcursorfilter(v=EXCHG.10)
ms:contentKeyID: 55104447
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetCursorFilter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0137c25ee6ab548537d797af0a00a7ffcd1f6d5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308796"
---
# <a name="windows8apijetsetcursorfilter-method"></a><span data-ttu-id="e4ed1-103">Windows8Api. JetSetCursorFilter, metodo</span><span class="sxs-lookup"><span data-stu-id="e4ed1-103">Windows8Api.JetSetCursorFilter method</span></span>

<span data-ttu-id="e4ed1-104">Impostare una matrice di filtri semplici per [JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span><span class="sxs-lookup"><span data-stu-id="e4ed1-104">Set an array of simple filters for [JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)](./api.jetmove-method-jet-sesid-jet-tableid-int32-movegrbit-.md).</span></span>

<span data-ttu-id="e4ed1-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4ed1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="e4ed1-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e4ed1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ed1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e4ed1-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCursorFilter ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    filters As JET_INDEX_COLUMN(), _
    grbit As CursorFilterGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim filters As JET_INDEX_COLUMN()
Dim grbit As CursorFilterGrbitWindows8Api.JetSetCursorFilter(sesid, tableid, _
    filters, grbit)
```

``` csharp
public static void JetSetCursorFilter(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_COLUMN[] filters,
    CursorFilterGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e4ed1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e4ed1-108">Parameters</span></span>

  - <span data-ttu-id="e4ed1-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e4ed1-109">sesid</span></span>  
    <span data-ttu-id="e4ed1-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4ed1-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e4ed1-111">Sessione da utilizzare per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="e4ed1-111">The session to use for the call.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4ed1-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e4ed1-112">tableid</span></span>  
    <span data-ttu-id="e4ed1-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e4ed1-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e4ed1-114">Cursore da posizionare.</span><span class="sxs-lookup"><span data-stu-id="e4ed1-114">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4ed1-115">filters</span><span class="sxs-lookup"><span data-stu-id="e4ed1-115">filters</span></span>  
    <span data-ttu-id="e4ed1-116">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="e4ed1-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="e4ed1-117">Filtri di record semplici.</span><span class="sxs-lookup"><span data-stu-id="e4ed1-117">Simple record filters.</span></span>

<!-- end list -->

  - <span data-ttu-id="e4ed1-118">grbit</span><span class="sxs-lookup"><span data-stu-id="e4ed1-118">grbit</span></span>  
    <span data-ttu-id="e4ed1-119">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e4ed1-119">Type: [Microsoft.Isam.Esent.Interop.Windows8.CursorFilterGrbit](./cursorfiltergrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e4ed1-120">Opzioni di spostamento.</span><span class="sxs-lookup"><span data-stu-id="e4ed1-120">Move options.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4ed1-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e4ed1-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4ed1-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e4ed1-122">Reference</span></span>

[<span data-ttu-id="e4ed1-123">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="e4ed1-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="e4ed1-124">Membri di Windows8Api</span><span class="sxs-lookup"><span data-stu-id="e4ed1-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="e4ed1-125">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="e4ed1-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
