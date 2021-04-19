---
description: 'Altre informazioni su: metodo API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Metodo API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnsize(v=EXCHG.10)
ms:contentKeyID: 55100868
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
ms.openlocfilehash: 6f75ce51e942cfde7fddc4f9ec0154feae985e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318467"
---
# <a name="apiretrievecolumnsize-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="42812-103">Metodo API. RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="42812-103">Api.RetrieveColumnSize method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="42812-104">Recupera le dimensioni di un valore di colonna singola dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="42812-104">Retrieves the size of a single column value from the current record.</span></span> <span data-ttu-id="42812-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="42812-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="42812-106">In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore.</span><span class="sxs-lookup"><span data-stu-id="42812-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="42812-107">Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente.</span><span class="sxs-lookup"><span data-stu-id="42812-107">This function can also retrieve column data from an index entry that references the current record.</span></span>

<span data-ttu-id="42812-108">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="42812-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="42812-109">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="42812-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="42812-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42812-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnSize(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<int> RetrieveColumnSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="42812-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="42812-111">Parameters</span></span>

  - <span data-ttu-id="42812-112">sesid</span><span class="sxs-lookup"><span data-stu-id="42812-112">sesid</span></span>  
    <span data-ttu-id="42812-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="42812-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="42812-114">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="42812-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="42812-115">TableID</span><span class="sxs-lookup"><span data-stu-id="42812-115">tableid</span></span>  
    <span data-ttu-id="42812-116">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="42812-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="42812-117">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="42812-117">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="42812-118">columnid</span><span class="sxs-lookup"><span data-stu-id="42812-118">columnid</span></span>  
    <span data-ttu-id="42812-119">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="42812-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="42812-120">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="42812-120">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="42812-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42812-121">Return value</span></span>

<span data-ttu-id="42812-122">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="42812-122">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="42812-123">Dimensione della colonna.</span><span class="sxs-lookup"><span data-stu-id="42812-123">The size of the column.</span></span> <span data-ttu-id="42812-124">0 se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="42812-124">0 if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="42812-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42812-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="42812-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="42812-126">Reference</span></span>

[<span data-ttu-id="42812-127">Classe API</span><span class="sxs-lookup"><span data-stu-id="42812-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="42812-128">Membri API</span><span class="sxs-lookup"><span data-stu-id="42812-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="42812-129">Overload RetrieveColumnSize</span><span class="sxs-lookup"><span data-stu-id="42812-129">RetrieveColumnSize overload</span></span>](./api.retrievecolumnsize-method.md)

[<span data-ttu-id="42812-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="42812-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
