---
description: 'Altre informazioni su: metodo API. MakeKey (JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)'
title: Metodo API. MakeKey (JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.DateTime,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100818
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9bbb710d6257deaf8c3467d33c2fd2aa11d22cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884429"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-datetime-makekeygrbit"></a><span data-ttu-id="1237c-103">Metodo API. MakeKey (JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="1237c-103">Api.MakeKey method (JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)</span></span>

<span data-ttu-id="1237c-104">Costruisce una chiave di ricerca che può quindi essere usata da [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) e [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="1237c-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="1237c-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1237c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1237c-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1237c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1237c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1237c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As DateTime, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As DateTime
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    DateTime data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1237c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1237c-108">Parameters</span></span>

  - <span data-ttu-id="1237c-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1237c-109">sesid</span></span>  
    <span data-ttu-id="1237c-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1237c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1237c-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="1237c-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1237c-112">TableID</span><span class="sxs-lookup"><span data-stu-id="1237c-112">tableid</span></span>  
    <span data-ttu-id="1237c-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1237c-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1237c-114">Cursore su cui creare la chiave.</span><span class="sxs-lookup"><span data-stu-id="1237c-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="1237c-115">data</span><span class="sxs-lookup"><span data-stu-id="1237c-115">data</span></span>  
    <span data-ttu-id="1237c-116">Tipo: [System. DateTime](/dotnet/api/system.datetime)</span><span class="sxs-lookup"><span data-stu-id="1237c-116">Type: [System.DateTime](/dotnet/api/system.datetime)</span></span>  
    
    <span data-ttu-id="1237c-117">Dati della colonna chiave corrente dell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="1237c-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="1237c-118">grbit</span><span class="sxs-lookup"><span data-stu-id="1237c-118">grbit</span></span>  
    <span data-ttu-id="1237c-119">Tipo: [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1237c-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1237c-120">Opzioni chiave.</span><span class="sxs-lookup"><span data-stu-id="1237c-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1237c-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1237c-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1237c-122">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1237c-122">Reference</span></span>

[<span data-ttu-id="1237c-123">Classe API</span><span class="sxs-lookup"><span data-stu-id="1237c-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1237c-124">Membri API</span><span class="sxs-lookup"><span data-stu-id="1237c-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1237c-125">Overload MakeKey</span><span class="sxs-lookup"><span data-stu-id="1237c-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="1237c-126">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1237c-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
