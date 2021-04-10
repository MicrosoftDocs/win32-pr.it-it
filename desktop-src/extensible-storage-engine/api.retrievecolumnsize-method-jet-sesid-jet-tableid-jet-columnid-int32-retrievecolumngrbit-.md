---
description: 'Altre informazioni su: metodo API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)'
title: Metodo API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100912
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afd09ecca0362487d6c8e78f8e7c8d943f2f3269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966415"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid-int32-retrievecolumngrbit"></a><span data-ttu-id="61532-103">Metodo API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="61532-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="61532-104">Recupera le dimensioni di un valore di colonna singola dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="61532-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="61532-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="61532-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="61532-106">In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore.</span><span class="sxs-lookup"><span data-stu-id="61532-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="61532-107">Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente.</span><span class="sxs-lookup"><span data-stu-id="61532-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="61532-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="61532-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="61532-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="61532-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="61532-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61532-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    itagSequence As Integer, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim itagSequence As Integer
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid, itagSequence, _
    grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int itagSequence,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="61532-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="61532-111">Parameters</span></span>

  - <span data-ttu-id="61532-112">sesid</span><span class="sxs-lookup"><span data-stu-id="61532-112">sesid</span></span>  
    <span data-ttu-id="61532-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="61532-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="61532-114">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="61532-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="61532-115">TableID</span><span class="sxs-lookup"><span data-stu-id="61532-115">tableid</span></span>  
    <span data-ttu-id="61532-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="61532-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="61532-117">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="61532-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="61532-118">columnid</span><span class="sxs-lookup"><span data-stu-id="61532-118">columnid</span></span>  
    <span data-ttu-id="61532-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="61532-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="61532-120">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="61532-120">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="61532-121">itagSequence</span><span class="sxs-lookup"><span data-stu-id="61532-121">itagSequence</span></span>  
    <span data-ttu-id="61532-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="61532-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="61532-123">Numero di sequenza del valore in una colonna multivalore.</span><span class="sxs-lookup"><span data-stu-id="61532-123">The sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="61532-124">La matrice di valori è in base uno.</span><span class="sxs-lookup"><span data-stu-id="61532-124">The array of values is one-based.</span></span> <span data-ttu-id="61532-125">Il primo valore è Sequence 1, not 0.</span><span class="sxs-lookup"><span data-stu-id="61532-125">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="61532-126">Se la colonna record ha un solo valore, è necessario passare 1 come itagSequence.</span><span class="sxs-lookup"><span data-stu-id="61532-126">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<!-- end list -->

  - <span data-ttu-id="61532-127">grbit</span><span class="sxs-lookup"><span data-stu-id="61532-127">grbit</span></span>  
    <span data-ttu-id="61532-128">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="61532-128">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="61532-129">Recupera le opzioni della colonna.</span><span class="sxs-lookup"><span data-stu-id="61532-129">Retrieve column options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="61532-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="61532-130">Return value</span></span>

<span data-ttu-id="61532-131">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="61532-131">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="61532-132">Dimensione della colonna.</span><span class="sxs-lookup"><span data-stu-id="61532-132">The size of the column.</span></span> <span data-ttu-id="61532-133">0 se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="61532-133">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="61532-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="61532-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="61532-135">Riferimento</span><span class="sxs-lookup"><span data-stu-id="61532-135">Reference</span></span>

[<span data-ttu-id="61532-136">Classe API</span><span class="sxs-lookup"><span data-stu-id="61532-136">Api class</span></span>](./api-class.md)

[<span data-ttu-id="61532-137">Membri API</span><span class="sxs-lookup"><span data-stu-id="61532-137">Api members</span></span>](./api-members.md)

[<span data-ttu-id="61532-138">Overload RetrieveColumnSize</span><span class="sxs-lookup"><span data-stu-id="61532-138">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="61532-139">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="61532-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
