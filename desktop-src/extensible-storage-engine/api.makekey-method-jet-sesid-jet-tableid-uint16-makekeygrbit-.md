---
description: 'Altre informazioni su: metodo API. MakeKey (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)'
title: Metodo API. MakeKey (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.UInt16,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100844
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
ms.openlocfilehash: 41df8909993b6c274d1a85737b13c2f618bc8fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318466"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-uint16-makekeygrbit"></a><span data-ttu-id="ed27e-103">Metodo API. MakeKey (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</span><span class="sxs-lookup"><span data-stu-id="ed27e-103">Api.MakeKey method (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</span></span>

<span data-ttu-id="ed27e-104">Costruisce una chiave di ricerca che può quindi essere usata da [JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) e [JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="ed27e-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="ed27e-105">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="ed27e-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="ed27e-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ed27e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ed27e-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ed27e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ed27e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed27e-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As UShort, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As UShort
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ushort data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ed27e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed27e-109">Parameters</span></span>

  - <span data-ttu-id="ed27e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="ed27e-110">sesid</span></span>  
    <span data-ttu-id="ed27e-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ed27e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ed27e-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ed27e-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ed27e-113">TableID</span><span class="sxs-lookup"><span data-stu-id="ed27e-113">tableid</span></span>  
    <span data-ttu-id="ed27e-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ed27e-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ed27e-115">Cursore su cui creare la chiave.</span><span class="sxs-lookup"><span data-stu-id="ed27e-115">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="ed27e-116">data</span><span class="sxs-lookup"><span data-stu-id="ed27e-116">data</span></span>  
    <span data-ttu-id="ed27e-117">Tipo: [System. UInt16](/dotnet/api/system.uint16)</span><span class="sxs-lookup"><span data-stu-id="ed27e-117">Type: [System.UInt16](/dotnet/api/system.uint16)</span></span>  
    
    <span data-ttu-id="ed27e-118">Dati della colonna chiave corrente dell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="ed27e-118">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="ed27e-119">grbit</span><span class="sxs-lookup"><span data-stu-id="ed27e-119">grbit</span></span>  
    <span data-ttu-id="ed27e-120">Tipo: [Microsoft. ISAM. esent. Interop. MakeKeyGrbit](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ed27e-120">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ed27e-121">Opzioni chiave.</span><span class="sxs-lookup"><span data-stu-id="ed27e-121">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="ed27e-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed27e-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ed27e-123">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ed27e-123">Reference</span></span>

[<span data-ttu-id="ed27e-124">Classe API</span><span class="sxs-lookup"><span data-stu-id="ed27e-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ed27e-125">Membri API</span><span class="sxs-lookup"><span data-stu-id="ed27e-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ed27e-126">Overload MakeKey</span><span class="sxs-lookup"><span data-stu-id="ed27e-126">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="ed27e-127">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ed27e-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
