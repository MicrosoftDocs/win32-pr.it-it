---
description: 'Altre informazioni su: metodo API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)'
title: Metodo API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100853
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43657ec60e521795ba4d474306de9380618cd21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305559"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="58b38-103">Metodo API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="58b38-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="58b38-104">Recupera un valore di colonna singola dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="58b38-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="58b38-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="58b38-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="58b38-106">In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore.</span><span class="sxs-lookup"><span data-stu-id="58b38-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="58b38-107">Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente.</span><span class="sxs-lookup"><span data-stu-id="58b38-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="58b38-108">Oltre a recuperare il valore della colonna effettivo, è possibile utilizzare JetRetrieveColumn anche per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="58b38-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="58b38-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="58b38-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="58b38-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="58b38-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="58b38-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58b38-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid, grbit, retinfo)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="58b38-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="58b38-112">Parameters</span></span>

  - <span data-ttu-id="58b38-113">sesid</span><span class="sxs-lookup"><span data-stu-id="58b38-113">sesid</span></span>  
    <span data-ttu-id="58b38-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="58b38-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="58b38-115">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="58b38-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="58b38-116">TableID</span><span class="sxs-lookup"><span data-stu-id="58b38-116">tableid</span></span>  
    <span data-ttu-id="58b38-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="58b38-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="58b38-118">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="58b38-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="58b38-119">columnid</span><span class="sxs-lookup"><span data-stu-id="58b38-119">columnid</span></span>  
    <span data-ttu-id="58b38-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="58b38-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="58b38-121">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="58b38-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="58b38-122">grbit</span><span class="sxs-lookup"><span data-stu-id="58b38-122">grbit</span></span>  
    <span data-ttu-id="58b38-123">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="58b38-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="58b38-124">Recupera le opzioni della colonna.</span><span class="sxs-lookup"><span data-stu-id="58b38-124">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="58b38-125">retinfo</span><span class="sxs-lookup"><span data-stu-id="58b38-125">retinfo</span></span>  
    <span data-ttu-id="58b38-126">Tipo: [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="58b38-126">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="58b38-127">Se pretinfo viene fornito come NULL, la funzione si comporta come se fosse stato specificato un itagSequence di 1 e un ibLongValue di 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="58b38-127">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="58b38-128">In questo modo il recupero della colonna Recupera il primo valore di una colonna multivalore e recupera i dati lunghi in corrispondenza dell'offset 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="58b38-128">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="58b38-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58b38-129">Return value</span></span>

<span data-ttu-id="58b38-130">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="58b38-130">Type: \[\]</span></span>  
<span data-ttu-id="58b38-131">Dati recuperati dalla colonna.</span><span class="sxs-lookup"><span data-stu-id="58b38-131">The data retrieved from the column.</span></span> <span data-ttu-id="58b38-132">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="58b38-132">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="58b38-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58b38-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="58b38-134">Riferimento</span><span class="sxs-lookup"><span data-stu-id="58b38-134">Reference</span></span>

[<span data-ttu-id="58b38-135">Classe API</span><span class="sxs-lookup"><span data-stu-id="58b38-135">Api class</span></span>](./api-class.md)

[<span data-ttu-id="58b38-136">Membri API</span><span class="sxs-lookup"><span data-stu-id="58b38-136">Api members</span></span>](./api-members.md)

[<span data-ttu-id="58b38-137">Overload RetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="58b38-137">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="58b38-138">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="58b38-138">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
