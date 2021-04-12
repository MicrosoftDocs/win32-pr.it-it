---
description: 'Altre informazioni su: metodo API. JetUpdate (JET_SESID, JET_TABLEID)'
title: Metodo API. JetUpdate (JET_SESID, JET_TABLEID)
TOCTitle: JetUpdate method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetupdate(v=EXCHG.10)
ms:contentKeyID: 55100831
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
ms.openlocfilehash: f1875353e8a5b4a23302a5f008af2cfa42a89b11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349586"
---
# <a name="apijetupdate-method-jet_sesid-jet_tableid"></a><span data-ttu-id="25919-103">Metodo API. JetUpdate (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="25919-103">Api.JetUpdate method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="25919-104">La funzione JetUpdate esegue un'operazione di aggiornamento, incluso l'inserimento di una nuova riga in una tabella o l'aggiornamento di una riga esistente.</span><span class="sxs-lookup"><span data-stu-id="25919-104">The JetUpdate function performs an update operation including inserting a new row into a table or updating an existing row.</span></span> <span data-ttu-id="25919-105">L'eliminazione di una riga di tabella viene eseguita chiamando [JetDelete (JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span><span class="sxs-lookup"><span data-stu-id="25919-105">Deleting a table row is performed by calling [JetDelete(JET_SESID, JET_TABLEID)](./api.jetdelete-method.md).</span></span>

<span data-ttu-id="25919-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25919-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25919-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25919-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25919-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25919-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEIDApi.JetUpdate(sesid, tableid)
```

``` csharp
public static void JetUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="25919-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="25919-109">Parameters</span></span>

  - <span data-ttu-id="25919-110">sesid</span><span class="sxs-lookup"><span data-stu-id="25919-110">sesid</span></span>  
    <span data-ttu-id="25919-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25919-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="25919-112">Sessione che ha avviato l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="25919-112">The session which started the update.</span></span>

<!-- end list -->

  - <span data-ttu-id="25919-113">TableID</span><span class="sxs-lookup"><span data-stu-id="25919-113">tableid</span></span>  
    <span data-ttu-id="25919-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25919-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="25919-115">Cursore da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="25919-115">The cursor to update.</span></span> <span data-ttu-id="25919-116">È necessario preparare un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="25919-116">An update should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="25919-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="25919-117">Remarks</span></span>

<span data-ttu-id="25919-118">JetUpdate è il passaggio finale per eseguire un inserimento o un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="25919-118">JetUpdate is the final step in performing an insert or an update.</span></span> <span data-ttu-id="25919-119">L'aggiornamento viene avviato chiamando [JetPrepareUpdate (JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) e quindi chiamando [JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) una o più volte per impostare lo stato del record.</span><span class="sxs-lookup"><span data-stu-id="25919-119">The update is begun by calling [JetPrepareUpdate(JET_SESID, JET_TABLEID, JET_prep)](./api.jetprepareupdate-method.md) and then by calling [JetSetColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, SetColumnGrbit, JET_SETINFO)](./api.jetsetcolumn-method-jet-sesid-jet-tableid-jet-columnid-byte-int32-setcolumngrbit-jet-setinfo-.md) one or more times to set the record state.</span></span> <span data-ttu-id="25919-120">Infine, [JetUpdate (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) viene chiamato per completare l'operazione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="25919-120">Finally, [JetUpdate(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetupdate-method-jet-sesid-jet-tableid-byte-int32-int32-.md) is called to complete the update operation.</span></span> <span data-ttu-id="25919-121">Gli indici vengono aggiornati solo da JetUpdate o e non durante JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="25919-121">Indexes are updated only by JetUpdate or and not during JetSetColumn.</span></span>

## <a name="see-also"></a><span data-ttu-id="25919-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25919-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25919-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="25919-123">Reference</span></span>

[<span data-ttu-id="25919-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="25919-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="25919-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="25919-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="25919-126">Overload JetUpdate</span><span class="sxs-lookup"><span data-stu-id="25919-126">JetUpdate overload</span></span>](./api.jetupdate-method.md)

[<span data-ttu-id="25919-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="25919-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
