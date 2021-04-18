---
description: 'Altre informazioni su: JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315116"
---
# <a name="jet_ls"></a><span data-ttu-id="905db-103">JET_LS</span><span class="sxs-lookup"><span data-stu-id="905db-103">JET_LS</span></span>


<span data-ttu-id="905db-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="905db-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_ls"></a><span data-ttu-id="905db-105">JET_LS</span><span class="sxs-lookup"><span data-stu-id="905db-105">JET_LS</span></span>

<span data-ttu-id="905db-106">Il tipo di dati **JET_LS** contiene un handle di contesto per l'archiviazione locale (ls). Questo handle può essere associato a un cursore o a una tabella e può fare riferimento a risorse allocate in modo dinamico.</span><span class="sxs-lookup"><span data-stu-id="905db-106">The **JET_LS** data type contains a context handle to local storage (LS).This handle might be associated with a cursor or a table and might refer to dynamically allocated resources.</span></span>

<span data-ttu-id="905db-107">**Windows XP: JET_LS** è stato introdotto in Windows XP.</span><span class="sxs-lookup"><span data-stu-id="905db-107">**Windows XP:  JET_LS** is introduced in Windows XP.</span></span>

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a><span data-ttu-id="905db-108">Tipi di dati</span><span class="sxs-lookup"><span data-stu-id="905db-108">Data Types</span></span>

<span data-ttu-id="905db-109">JET_LS</span><span class="sxs-lookup"><span data-stu-id="905db-109">JET_LS</span></span>

<span data-ttu-id="905db-110">Il valore JET_LSNil indica un handle di contesto non valido.</span><span class="sxs-lookup"><span data-stu-id="905db-110">A value of JET_LSNil indicates an invalid context handle.</span></span>

### <a name="remarks"></a><span data-ttu-id="905db-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="905db-111">Remarks</span></span>

<span data-ttu-id="905db-112">Un handle di contesto viene inizialmente associato al tipo di dati **JET_LS** , usando [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="905db-112">A context handle is initially associated with the **JET_LS** data type, using [JetSetLS](./jetsetls-function.md).</span></span> <span data-ttu-id="905db-113">L'handle di contesto può essere recuperato dal tipo di dati **JET_LS** , usando [JetGetLS](./jetgetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="905db-113">The context handle can be retrieved from the **JET_LS** data type, using [JetGetLS](./jetgetls-function.md).</span></span>

<span data-ttu-id="905db-114">È possibile dissociare in modo esplicito l'handle del contesto dal tipo di dati **JET_LS** usando [JetGetLS](./jetgetls-function.md) con JET_bitLSReset.</span><span class="sxs-lookup"><span data-stu-id="905db-114">The context handle can be explicitly disassociated from the **JET_LS** data type using [JetGetLS](./jetgetls-function.md) with JET_bitLSReset.</span></span> <span data-ttu-id="905db-115">In alternativa, l'handle di contesto può essere dissociato in modo implicito dal tipo di dati **JET_LS** quando l'oggetto sottostante viene rilasciato dal motore di database in seguito a un'azione diretta o indiretta da parte dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="905db-115">Alternatively, the context handle can be implicitly disassociated from the **JET_LS** data type when the underlying object is released by the database engine as a result of direct or indirect action by the application.</span></span> <span data-ttu-id="905db-116">Nel caso implicito, un callback di runtime viene emesso all'applicazione in modo che possa pulire l'handle del contesto.</span><span class="sxs-lookup"><span data-stu-id="905db-116">In the implicit case, a runtime callback is issued to the application so that it can clean up the context handle.</span></span> <span data-ttu-id="905db-117">Per ulteriori informazioni sulla disassociazione implicita dal tipo di dati **JET_LS** , vedere [JetSetLS](./jetsetls-function.md).</span><span class="sxs-lookup"><span data-stu-id="905db-117">For more information on implicitly disassociating from the **JET_LS** data type, see [JetSetLS](./jetsetls-function.md).</span></span>

<span data-ttu-id="905db-118">I flag seguenti sono associati al tipo di dati JET_LS.</span><span class="sxs-lookup"><span data-stu-id="905db-118">The following flags are associated with the JET_LS data type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="905db-119">Termine</span><span class="sxs-lookup"><span data-stu-id="905db-119">Term</span></span></p></th>
<th><p><span data-ttu-id="905db-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="905db-120">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="905db-121">JET_bitLSReset</span><span class="sxs-lookup"><span data-stu-id="905db-121">JET_bitLSReset</span></span></p></td>
<td><p><span data-ttu-id="905db-122">L'handle del contesto è dissociato dall'oggetto.</span><span class="sxs-lookup"><span data-stu-id="905db-122">The context handle is disassociated from the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="905db-123">JET_bitLSCursor</span><span class="sxs-lookup"><span data-stu-id="905db-123">JET_bitLSCursor</span></span></p></td>
<td><p><span data-ttu-id="905db-124">Impostare o recuperare lo spazio di archiviazione locale associato a un cursore della tabella.</span><span class="sxs-lookup"><span data-stu-id="905db-124">Set or retrieve the local storage associated with a table cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="905db-125">JET_bitLSTable</span><span class="sxs-lookup"><span data-stu-id="905db-125">JET_bitLSTable</span></span></p></td>
<td><p><span data-ttu-id="905db-126">Impostare o recuperare lo spazio di archiviazione locale associato a una tabella.</span><span class="sxs-lookup"><span data-stu-id="905db-126">Set or retrieve the local storage associated with a table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="905db-127">JET_LSNil</span><span class="sxs-lookup"><span data-stu-id="905db-127">JET_LSNil</span></span></p></td>
<td><p><span data-ttu-id="905db-128">Handle di contesto non valido.</span><span class="sxs-lookup"><span data-stu-id="905db-128">The context handle is invalid.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="905db-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="905db-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="905db-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="905db-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="905db-131">Richiede Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="905db-131">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="905db-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="905db-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="905db-133">Richiede Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="905db-133">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="905db-134"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="905db-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="905db-135">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="905db-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="905db-136">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="905db-136">See Also</span></span>

[<span data-ttu-id="905db-137">JetSetLS</span><span class="sxs-lookup"><span data-stu-id="905db-137">JetSetLS</span></span>](./jetsetls-function.md)  
[<span data-ttu-id="905db-138">JetGetLS</span><span class="sxs-lookup"><span data-stu-id="905db-138">JetGetLS</span></span>](./jetgetls-function.md)
