---
description: 'Altre informazioni su: metodo API. MakeKey (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)'
title: Metodo API. MakeKey (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,System.Text.Encoding,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100830
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
ms.openlocfilehash: d5f4fa9dfd848ff6aef858533501891e08ef8972
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308578"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-string-encoding-makekeygrbit"></a><span data-ttu-id="7a9d3-103">Metodo API. MakeKey (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-103">Api.MakeKey method (JET_SESID, JET_TABLEID, String, Encoding, MakeKeyGrbit)</span></span>

<span data-ttu-id="7a9d3-104">Costruisce una chiave di ricerca che può quindi essere usata da [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) e [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="7a9d3-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="7a9d3-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7a9d3-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a9d3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a9d3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As String, _
    encoding As Encoding, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As String
Dim encoding As Encoding
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    encoding, grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string data,
    Encoding encoding,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7a9d3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a9d3-108">Parameters</span></span>

  - <span data-ttu-id="7a9d3-109">sesid</span><span class="sxs-lookup"><span data-stu-id="7a9d3-109">sesid</span></span>  
    <span data-ttu-id="7a9d3-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7a9d3-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a9d3-112">TableID</span><span class="sxs-lookup"><span data-stu-id="7a9d3-112">tableid</span></span>  
    <span data-ttu-id="7a9d3-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7a9d3-114">Cursore su cui creare la chiave.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a9d3-115">data</span><span class="sxs-lookup"><span data-stu-id="7a9d3-115">data</span></span>  
    <span data-ttu-id="7a9d3-116">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7a9d3-117">Dati della colonna chiave corrente dell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a9d3-118">codifica</span><span class="sxs-lookup"><span data-stu-id="7a9d3-118">encoding</span></span>  
    <span data-ttu-id="7a9d3-119">Tipo: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-119">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="7a9d3-120">Codifica utilizzata per convertire la stringa.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-120">The encoding used to convert the string.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a9d3-121">grbit</span><span class="sxs-lookup"><span data-stu-id="7a9d3-121">grbit</span></span>  
    <span data-ttu-id="7a9d3-122">Tipo: [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7a9d3-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7a9d3-123">Opzioni chiave.</span><span class="sxs-lookup"><span data-stu-id="7a9d3-123">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a9d3-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a9d3-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a9d3-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7a9d3-125">Reference</span></span>

[<span data-ttu-id="7a9d3-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="7a9d3-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7a9d3-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="7a9d3-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7a9d3-128">Overload MakeKey</span><span class="sxs-lookup"><span data-stu-id="7a9d3-128">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="7a9d3-129">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7a9d3-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
