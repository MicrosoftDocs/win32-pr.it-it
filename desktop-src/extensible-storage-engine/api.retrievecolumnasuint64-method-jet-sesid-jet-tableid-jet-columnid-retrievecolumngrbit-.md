---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Metodo API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint64(v=EXCHG.10)
ms:contentKeyID: 55100907
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb4de0dc72493d0b28716b5a0859aa19adfe62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484165"
---
# <a name="apiretrievecolumnasuint64-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="178a6-103">Metodo API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="178a6-103">Api.RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="178a6-104">Recupera un valore di colonna UInt64 dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="178a6-104">Retrieves a uint64 column value from the current record.</span></span> <span data-ttu-id="178a6-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="178a6-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="178a6-106">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="178a6-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="178a6-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="178a6-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="178a6-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="178a6-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="178a6-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="178a6-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of ULong)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of ULong)

returnValue = Api.RetrieveColumnAsUInt64(sesid, _
    tableid, columnid, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ulong> RetrieveColumnAsUInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="178a6-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="178a6-110">Parameters</span></span>

  - <span data-ttu-id="178a6-111">sesid</span><span class="sxs-lookup"><span data-stu-id="178a6-111">sesid</span></span>  
    <span data-ttu-id="178a6-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="178a6-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="178a6-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="178a6-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="178a6-114">TableID</span><span class="sxs-lookup"><span data-stu-id="178a6-114">tableid</span></span>  
    <span data-ttu-id="178a6-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="178a6-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="178a6-116">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="178a6-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="178a6-117">columnid</span><span class="sxs-lookup"><span data-stu-id="178a6-117">columnid</span></span>  
    <span data-ttu-id="178a6-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="178a6-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="178a6-119">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="178a6-119">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="178a6-120">grbit</span><span class="sxs-lookup"><span data-stu-id="178a6-120">grbit</span></span>  
    <span data-ttu-id="178a6-121">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="178a6-121">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="178a6-122">Opzioni di recupero.</span><span class="sxs-lookup"><span data-stu-id="178a6-122">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="178a6-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="178a6-123">Return value</span></span>

<span data-ttu-id="178a6-124">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span><span class="sxs-lookup"><span data-stu-id="178a6-124">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span></span>  
<span data-ttu-id="178a6-125">Dati recuperati dalla colonna come UInt64.</span><span class="sxs-lookup"><span data-stu-id="178a6-125">The data retrieved from the column as an UInt64.</span></span> <span data-ttu-id="178a6-126">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="178a6-126">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="178a6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="178a6-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="178a6-128">Riferimento</span><span class="sxs-lookup"><span data-stu-id="178a6-128">Reference</span></span>

[<span data-ttu-id="178a6-129">Classe API</span><span class="sxs-lookup"><span data-stu-id="178a6-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="178a6-130">Membri API</span><span class="sxs-lookup"><span data-stu-id="178a6-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="178a6-131">Overload RetrieveColumnAsUInt64</span><span class="sxs-lookup"><span data-stu-id="178a6-131">RetrieveColumnAsUInt64 overload</span></span>](./api.retrievecolumnasuint64-method.md)

[<span data-ttu-id="178a6-132">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="178a6-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
