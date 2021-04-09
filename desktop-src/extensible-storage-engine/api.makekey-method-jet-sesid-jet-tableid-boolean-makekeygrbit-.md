---
description: 'Altre informazioni su: metodo API. MakeKey (JET_SESID, JET_TABLEID, booleano, MakeKeyGrbit)'
title: Metodo API. MakeKey (JET_SESID, JET_TABLEID, Boolean, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Boolean, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Boolean,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100834
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 83205a78b0d652edb4a8a6b08432f1f38257528e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879861"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-boolean-makekeygrbit"></a><span data-ttu-id="c9a8e-103">Metodo API. MakeKey (JET_SESID, JET_TABLEID, Boolean, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="c9a8e-103">Api.MakeKey method (JET_SESID, JET_TABLEID, Boolean, MakeKeyGrbit)</span></span>

<span data-ttu-id="c9a8e-104">Costruisce una chiave di ricerca che può quindi essere usata da [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) e [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="c9a8e-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="c9a8e-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c9a8e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c9a8e-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c9a8e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a8e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9a8e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Boolean, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Boolean
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    bool data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c9a8e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9a8e-108">Parameters</span></span>

  - <span data-ttu-id="c9a8e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="c9a8e-109">sesid</span></span>  
    <span data-ttu-id="c9a8e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9a8e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c9a8e-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9a8e-112">TableID</span><span class="sxs-lookup"><span data-stu-id="c9a8e-112">tableid</span></span>  
    <span data-ttu-id="c9a8e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c9a8e-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c9a8e-114">Cursore su cui creare la chiave.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9a8e-115">data</span><span class="sxs-lookup"><span data-stu-id="c9a8e-115">data</span></span>  
    <span data-ttu-id="c9a8e-116">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="c9a8e-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
    
    <span data-ttu-id="c9a8e-117">Dati della colonna chiave corrente dell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="c9a8e-118">grbit</span><span class="sxs-lookup"><span data-stu-id="c9a8e-118">grbit</span></span>  
    <span data-ttu-id="c9a8e-119">Tipo: [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c9a8e-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c9a8e-120">Opzioni chiave.</span><span class="sxs-lookup"><span data-stu-id="c9a8e-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9a8e-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9a8e-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c9a8e-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c9a8e-122">Reference</span></span>

[<span data-ttu-id="c9a8e-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="c9a8e-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c9a8e-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="c9a8e-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c9a8e-125">Overload MakeKey</span><span class="sxs-lookup"><span data-stu-id="c9a8e-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="c9a8e-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c9a8e-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
