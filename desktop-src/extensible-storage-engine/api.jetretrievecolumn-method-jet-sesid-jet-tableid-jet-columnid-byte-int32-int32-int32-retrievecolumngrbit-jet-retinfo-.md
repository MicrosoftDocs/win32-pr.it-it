---
description: 'Altre informazioni su: metodo API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)'
title: Metodo API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
TOCTitle: JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit,Microsoft.Isam.Esent.Interop.JET_RETINFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100792
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832e6d6cc123e4a85a2cacb2df688348732fcc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349601"
---
# <a name="apijetretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid-byte--int32-int32-int32-retrievecolumngrbit-jet_retinfo"></a><span data-ttu-id="b6ac0-103">Metodo API. JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, byte, Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-103">Api.JetRetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte , Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</span></span>

<span data-ttu-id="b6ac0-104">Recupera un valore di colonna singola dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="b6ac0-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-105">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="b6ac0-106">In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-106">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="b6ac0-107">Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-107">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="b6ac0-108">Oltre a recuperare il valore della colonna effettivo, è possibile utilizzare JetRetrieveColumn anche per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-108">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span>

<span data-ttu-id="b6ac0-109">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b6ac0-110">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b6ac0-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6ac0-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    data As Byte(), _
    dataSize As Integer, _
    dataOffset As Integer, _
    <OutAttribute> ByRef actualDataSize As Integer, _
    grbit As RetrieveColumnGrbit, _
    retinfo As JET_RETINFO _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim data As Byte()
Dim dataSize As Integer
Dim dataOffset As Integer
Dim actualDataSize As Integer
Dim grbit As RetrieveColumnGrbit
Dim retinfo As JET_RETINFO
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumn(sesid, _
    tableid, columnid, data, dataSize, _
    dataOffset, actualDataSize, grbit, _
    retinfo)
```

``` csharp
public static JET_wrn JetRetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] data,
    int dataSize,
    int dataOffset,
    out int actualDataSize,
    RetrieveColumnGrbit grbit,
    JET_RETINFO retinfo
)
```

#### <a name="parameters"></a><span data-ttu-id="b6ac0-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="b6ac0-112">Parameters</span></span>

  - <span data-ttu-id="b6ac0-113">sesid</span><span class="sxs-lookup"><span data-stu-id="b6ac0-113">sesid</span></span>  
    <span data-ttu-id="b6ac0-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b6ac0-115">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6ac0-116">TableID</span><span class="sxs-lookup"><span data-stu-id="b6ac0-116">tableid</span></span>  
    <span data-ttu-id="b6ac0-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-117">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="b6ac0-118">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-118">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6ac0-119">columnid</span><span class="sxs-lookup"><span data-stu-id="b6ac0-119">columnid</span></span>  
    <span data-ttu-id="b6ac0-120">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-120">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="b6ac0-121">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-121">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6ac0-122">data</span><span class="sxs-lookup"><span data-stu-id="b6ac0-122">data</span></span>  
    <span data-ttu-id="b6ac0-123">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="b6ac0-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="b6ac0-124">Buffer di dati in cui recuperare.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-124">The data buffer to be retrieved into.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6ac0-125">dataSize</span><span class="sxs-lookup"><span data-stu-id="b6ac0-125">dataSize</span></span>  
    <span data-ttu-id="b6ac0-126">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b6ac0-127">Dimensioni del buffer di dati.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-127">The size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6ac0-128">dataOffset</span><span class="sxs-lookup"><span data-stu-id="b6ac0-128">dataOffset</span></span>  
    <span data-ttu-id="b6ac0-129">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-129">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b6ac0-130">Offset nel buffer dei dati in cui leggere i dati.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-130">Offset into the data buffer to read data into.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6ac0-131">actualDataSize</span><span class="sxs-lookup"><span data-stu-id="b6ac0-131">actualDataSize</span></span>  
    <span data-ttu-id="b6ac0-132">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-132">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="b6ac0-133">Restituisce le dimensioni effettive del buffer di dati.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-133">Returns the actual size of the data buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6ac0-134">grbit</span><span class="sxs-lookup"><span data-stu-id="b6ac0-134">grbit</span></span>  
    <span data-ttu-id="b6ac0-135">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-135">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="b6ac0-136">Recupera le opzioni della colonna.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-136">Retrieve column options.</span></span>

<!-- end list -->

  - <span data-ttu-id="b6ac0-137">retinfo</span><span class="sxs-lookup"><span data-stu-id="b6ac0-137">retinfo</span></span>  
    <span data-ttu-id="b6ac0-138">Tipo: [Microsoft.ISAM.esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-138">Type: [Microsoft.Isam.Esent.Interop.JET_RETINFO](./jet-retinfo-class.md)</span></span>  
    
    <span data-ttu-id="b6ac0-139">Se pretinfo viene fornito come NULL, la funzione si comporta come se fosse stato specificato un itagSequence di 1 e un ibLongValue di 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b6ac0-139">If pretinfo is give as NULL then the function behaves as though an itagSequence of 1 and an ibLongValue of 0 (zero) were given.</span></span> <span data-ttu-id="b6ac0-140">In questo modo il recupero della colonna Recupera il primo valore di una colonna multivalore e recupera i dati lunghi in corrispondenza dell'offset 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="b6ac0-140">This causes column retrieval to retrieve the first value of a multi-valued column, and to retrieve long data at offset 0 (zero).</span></span>

#### <a name="return-value"></a><span data-ttu-id="b6ac0-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b6ac0-141">Return value</span></span>

<span data-ttu-id="b6ac0-142">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="b6ac0-142">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="b6ac0-143">Codice di avviso ESENT.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-143">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="b6ac0-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="b6ac0-144">Remarks</span></span>

<span data-ttu-id="b6ac0-145">Si tratta di un metodo interno che accetta un offset del buffer e le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="b6ac0-145">This is an internal method that takes a buffer offset as well as size.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6ac0-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6ac0-146">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b6ac0-147">Riferimento</span><span class="sxs-lookup"><span data-stu-id="b6ac0-147">Reference</span></span>

[<span data-ttu-id="b6ac0-148">Classe API</span><span class="sxs-lookup"><span data-stu-id="b6ac0-148">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b6ac0-149">Membri API</span><span class="sxs-lookup"><span data-stu-id="b6ac0-149">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b6ac0-150">Overload JetRetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="b6ac0-150">JetRetrieveColumn overload</span></span>](./api.jetretrievecolumn-method.md)

[<span data-ttu-id="b6ac0-151">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b6ac0-151">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
