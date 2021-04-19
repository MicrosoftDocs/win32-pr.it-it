---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Metodo API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint64(v=EXCHG.10)
ms:contentKeyID: 55100891
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 158e350dc3d85b99b4651c448c8b1b7d51a1ce14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317529"
---
# <a name="apiretrievecolumnasint64-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="5886a-103">Metodo API. RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="5886a-103">Api.RetrieveColumnAsInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="5886a-104">Recupera un valore di colonna singola dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="5886a-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="5886a-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="5886a-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="5886a-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5886a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5886a-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5886a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5886a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5886a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Long)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Long)

returnValue = Api.RetrieveColumnAsInt64(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<long> RetrieveColumnAsInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="5886a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5886a-109">Parameters</span></span>

  - <span data-ttu-id="5886a-110">sesid</span><span class="sxs-lookup"><span data-stu-id="5886a-110">sesid</span></span>  
    <span data-ttu-id="5886a-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5886a-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="5886a-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="5886a-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="5886a-113">TableID</span><span class="sxs-lookup"><span data-stu-id="5886a-113">tableid</span></span>  
    <span data-ttu-id="5886a-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5886a-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="5886a-115">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="5886a-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="5886a-116">columnid</span><span class="sxs-lookup"><span data-stu-id="5886a-116">columnid</span></span>  
    <span data-ttu-id="5886a-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="5886a-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="5886a-118">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5886a-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="5886a-119">grbit</span><span class="sxs-lookup"><span data-stu-id="5886a-119">grbit</span></span>  
    <span data-ttu-id="5886a-120">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5886a-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="5886a-121">Opzioni di recupero.</span><span class="sxs-lookup"><span data-stu-id="5886a-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5886a-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5886a-122">Return value</span></span>

<span data-ttu-id="5886a-123">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span><span class="sxs-lookup"><span data-stu-id="5886a-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int64](/dotnet/api/system.int64)\></span></span>  
<span data-ttu-id="5886a-124">Dati recuperati dalla colonna come Long.</span><span class="sxs-lookup"><span data-stu-id="5886a-124">The data retrieved from the column as a long.</span></span> <span data-ttu-id="5886a-125">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="5886a-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5886a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5886a-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5886a-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="5886a-127">Reference</span></span>

[<span data-ttu-id="5886a-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="5886a-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="5886a-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="5886a-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="5886a-130">Overload RetrieveColumnAsInt64</span><span class="sxs-lookup"><span data-stu-id="5886a-130">RetrieveColumnAsInt64 overload</span></span>](./api.retrievecolumnasint64-method.md)

[<span data-ttu-id="5886a-131">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="5886a-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
