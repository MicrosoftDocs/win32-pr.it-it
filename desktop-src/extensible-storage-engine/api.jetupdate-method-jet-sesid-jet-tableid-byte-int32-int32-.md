---
description: 'Altre informazioni su: metodo API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)'
title: Metodo API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100814
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUpdate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c85e424fc9b672944801da3d03cbaff0ca48017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879862"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid-byte--int32-int32"></a><span data-ttu-id="bdd1e-103">Metodo API. JetUpdate (JET_SESID, JET_TABLEID, byte, Int32, Int32)</span><span class="sxs-lookup"><span data-stu-id="bdd1e-103">Api.JetUpdate method (JET_SESID, JET_TABLEID, Byte , Int32, Int32)</span></span>

<span data-ttu-id="bdd1e-104">La funzione JetUpdate esegue un'operazione di aggiornamento, incluso l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="bdd1e-105">L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="bdd1e-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="bdd1e-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bdd1e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bdd1e-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bdd1e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd1e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdd1e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetUpdate(sesid, tableid, bookmark, _
    bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="bdd1e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdd1e-109">Parameters</span></span>

  - <span data-ttu-id="bdd1e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="bdd1e-110">sesid</span></span>  
    <span data-ttu-id="bdd1e-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bdd1e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="bdd1e-112">Sessione che ha avviato l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="bdd1e-113">TableID</span><span class="sxs-lookup"><span data-stu-id="bdd1e-113">tableid</span></span>  
    <span data-ttu-id="bdd1e-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="bdd1e-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="bdd1e-115">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-115">The cursor to update.</span></span> <span data-ttu-id="bdd1e-116">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-116">An update should be prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="bdd1e-117">segnalibro</span><span class="sxs-lookup"><span data-stu-id="bdd1e-117">bookmark</span></span>  
    <span data-ttu-id="bdd1e-118">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="bdd1e-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="bdd1e-119">Restituisce il segnalibro del record aggiornato.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-119">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="bdd1e-120">Può essere Null.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-120">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="bdd1e-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="bdd1e-121">bookmarkSize</span></span>  
    <span data-ttu-id="bdd1e-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bdd1e-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bdd1e-123">Dimensioni del buffer dei segnalibri.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-123">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="bdd1e-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="bdd1e-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="bdd1e-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="bdd1e-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="bdd1e-126">Restituisce le dimensioni effettive del segnalibro.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-126">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdd1e-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdd1e-127">Remarks</span></span>

<span data-ttu-id="bdd1e-128">JetUpdate è il passaggio finale per eseguire un inserimento o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-128">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="bdd1e-129">L'aggiornamento viene avviato chiamando [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) e quindi chiamando [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o più volte per impostare lo stato del record.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-129">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="bdd1e-130">Infine, JetUpdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32) viene chiamato per completare l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-130">Finally, JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32) is called to complete the update operation.</span></span> <span data-ttu-id="bdd1e-131">Gli indici vengono aggiornati solo da JetUpdate o e non durante JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="bdd1e-131">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="bdd1e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdd1e-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bdd1e-133">Riferimento</span><span class="sxs-lookup"><span data-stu-id="bdd1e-133">Reference</span></span>

[<span data-ttu-id="bdd1e-134">Classe API</span><span class="sxs-lookup"><span data-stu-id="bdd1e-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="bdd1e-135">Membri API</span><span class="sxs-lookup"><span data-stu-id="bdd1e-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="bdd1e-136">Overload JetUpdate</span><span class="sxs-lookup"><span data-stu-id="bdd1e-136">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="bdd1e-137">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bdd1e-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
