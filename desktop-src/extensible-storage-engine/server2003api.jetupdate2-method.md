---
description: 'Altre informazioni su: Server2003Api. JetUpdate2, metodo'
title: Metodo Server2003Api. JetUpdate2 (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: 'JetUpdate2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetupdate2(v=EXCHG.10)
ms:contentKeyID: 55104110
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetUpdate2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fff3687d42160df331bfe52660be232fe3b41d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128155"
---
# <a name="server2003apijetupdate2-method"></a><span data-ttu-id="90641-103">Server2003Api. JetUpdate2, metodo</span><span class="sxs-lookup"><span data-stu-id="90641-103">Server2003Api.JetUpdate2 method</span></span>

<span data-ttu-id="90641-104">La funzione JetUpdate esegue un'operazione di aggiornamento, incluso l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente.</span><span class="sxs-lookup"><span data-stu-id="90641-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="90641-105">L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="90641-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="90641-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="90641-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="90641-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="90641-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="90641-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="90641-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer, _
    grbit As UpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer
Dim grbit As UpdateGrbitServer2003Api.JetUpdate2(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize, _
    grbit)
```

``` csharp
public static void JetUpdate2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize,
    UpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="90641-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="90641-109">Parameters</span></span>

  - <span data-ttu-id="90641-110">sesid</span><span class="sxs-lookup"><span data-stu-id="90641-110">sesid</span></span>  
    <span data-ttu-id="90641-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="90641-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="90641-112">Sessione che ha avviato l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="90641-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="90641-113">TableID</span><span class="sxs-lookup"><span data-stu-id="90641-113">tableid</span></span>  
    <span data-ttu-id="90641-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="90641-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="90641-115">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="90641-115">The cursor to update.</span></span> <span data-ttu-id="90641-116">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="90641-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="90641-117">segnalibro</span><span class="sxs-lookup"><span data-stu-id="90641-117">bookmark</span></span>  
    <span data-ttu-id="90641-118">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="90641-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="90641-119">Restituisce il segnalibro del record aggiornato.</span><span class="sxs-lookup"><span data-stu-id="90641-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="90641-120">Può essere Null.</span><span class="sxs-lookup"><span data-stu-id="90641-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="90641-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="90641-121">bookmarkSize</span></span>  
    <span data-ttu-id="90641-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="90641-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="90641-123">Dimensioni del buffer dei segnalibri.</span><span class="sxs-lookup"><span data-stu-id="90641-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="90641-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="90641-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="90641-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="90641-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="90641-126">Restituisce le dimensioni effettive del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="90641-126">Returns the actual size of the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="90641-127">grbit</span><span class="sxs-lookup"><span data-stu-id="90641-127">grbit</span></span>  
    <span data-ttu-id="90641-128">Tipo: [Microsoft. ISAM. esent. Interop. Server2003. UpdateGrbit](./updategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="90641-128">Type: [Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit](./updategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="90641-129">Opzioni di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="90641-129">Update options.</span></span>

## <a name="remarks"></a><span data-ttu-id="90641-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="90641-130">Remarks</span></span>

<span data-ttu-id="90641-131">JetUpdate è il passaggio finale per eseguire un inserimento o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="90641-131">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="90641-132">L'aggiornamento viene avviato chiamando [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) e quindi chiamando [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o più volte per impostare lo stato del record.</span><span class="sxs-lookup"><span data-stu-id="90641-132">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="90641-133">Infine, \[ \] per completare l'operazione di aggiornamento viene chiamato JetUpdate2 (JET_SESID, JET_TABLEID,, Int32, Int32, UpdateGrbit).</span><span class="sxs-lookup"><span data-stu-id="90641-133">Finally, JetUpdate2(JET_SESID, JET_TABLEID, \[\], Int32, Int32, UpdateGrbit) is called to complete the update operation.</span></span> <span data-ttu-id="90641-134">Gli indici vengono aggiornati solo da JetUpdate o e non durante JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="90641-134">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="90641-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="90641-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="90641-136">Riferimento</span><span class="sxs-lookup"><span data-stu-id="90641-136">Reference</span></span>

[<span data-ttu-id="90641-137">Classe Server2003Api</span><span class="sxs-lookup"><span data-stu-id="90641-137">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="90641-138">Membri di Server2003Api</span><span class="sxs-lookup"><span data-stu-id="90641-138">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="90641-139">Spazio dei nomi Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="90641-139">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
