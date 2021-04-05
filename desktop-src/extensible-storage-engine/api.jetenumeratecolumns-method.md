---
description: 'Altre informazioni su: metodo API. JetEnumerateColumns'
title: API. JetEnumerateColumns, metodo
TOCTitle: 'JetEnumerateColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Int32,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID[],System.Int32@,Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN[]@,Microsoft.Isam.Esent.Interop.JET_PFNREALLOC,System.IntPtr,System.Int32,Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetenumeratecolumns(v=EXCHG.10)
ms:contentKeyID: 55100695
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEnumerateColumns
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c9a9848d4470d54cc2a146098343b664c9bd3419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049418"
---
# <a name="apijetenumeratecolumns-method"></a><span data-ttu-id="fbd7a-103">API. JetEnumerateColumns, metodo</span><span class="sxs-lookup"><span data-stu-id="fbd7a-103">Api.JetEnumerateColumns method</span></span>

<span data-ttu-id="fbd7a-104">Consente di recuperare in modo efficiente un set di colonne e i relativi valori dal record corrente di un cursore o dal buffer di copia del cursore.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-104">Efficiently retrieves a set of columns and their values from the current record of a cursor or the copy buffer of that cursor.</span></span> <span data-ttu-id="fbd7a-105">Le colonne e i valori recuperati possono essere limitati da un elenco di ID di colonna, numeri itagSequence e altre caratteristiche.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-105">The columns and values retrieved can be restricted by a list of column IDs, itagSequence numbers, and other characteristics.</span></span> <span data-ttu-id="fbd7a-106">Questa API di recupero colonne è univoca in quanto restituisce informazioni nella memoria allocata in modo dinamico, ottenuta usando un callback compatibile con realloc fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-106">This column retrieval API is unique in that it returns information in dynamically allocated memory that is obtained using a user-provided realloc compatible callback.</span></span> <span data-ttu-id="fbd7a-107">Questa nuova flessibilità consente di recuperare in modo efficiente i dati delle colonne con caratteristiche specifiche, ad esempio le dimensioni e la molteplicità, sconosciute al chiamante.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-107">This new flexibility permits the efficient retrieval of column data with specific characteristics (such as size and multiplicity) that are unknown to the caller.</span></span> <span data-ttu-id="fbd7a-108">In questo modo si elimina la necessità di usare le modalità di individuazione di JetRetrieveColumn per determinare tali caratteristiche per configurare una chiamata finale a JetRetrieveColumn che recupererà correttamente i dati desiderati.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-108">This eliminates the need for the use of the discovery modes of JetRetrieveColumn to determine those characteristics in order to setup a final call to JetRetrieveColumn that will successfully retrieve the desired data.</span></span>

<span data-ttu-id="fbd7a-109">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-109">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="fbd7a-110">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fbd7a-111">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd7a-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fbd7a-112">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function JetEnumerateColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    numColumnids As Integer, _
    columnids As JET_ENUMCOLUMNID(), _
    <OutAttribute> ByRef numColumnValues As Integer, _
    <OutAttribute> ByRef columnValues As JET_ENUMCOLUMN(), _
    allocator As JET_PFNREALLOC, _
    allocatorContext As IntPtr, _
    maxDataSize As Integer, _
    grbit As EnumerateColumnsGrbit _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim numColumnids As Integer
Dim columnids As JET_ENUMCOLUMNID()
Dim numColumnValues As Integer
Dim columnValues As JET_ENUMCOLUMN()
Dim allocator As JET_PFNREALLOC
Dim allocatorContext As IntPtr
Dim maxDataSize As Integer
Dim grbit As EnumerateColumnsGrbit
Dim returnValue As JET_wrn

returnValue = Api.JetEnumerateColumns(sesid, _
    tableid, numColumnids, columnids, _
    numColumnValues, columnValues, allocator, _
    allocatorContext, maxDataSize, grbit)
```

``` csharp
[CLSCompliantAttribute(false)]
public static JET_wrn JetEnumerateColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    int numColumnids,
    JET_ENUMCOLUMNID[] columnids,
    out int numColumnValues,
    out JET_ENUMCOLUMN[] columnValues,
    JET_PFNREALLOC allocator,
    IntPtr allocatorContext,
    int maxDataSize,
    EnumerateColumnsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="fbd7a-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="fbd7a-113">Parameters</span></span>

  - <span data-ttu-id="fbd7a-114">sesid</span><span class="sxs-lookup"><span data-stu-id="fbd7a-114">sesid</span></span>  
    <span data-ttu-id="fbd7a-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="fbd7a-116">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbd7a-117">TableID</span><span class="sxs-lookup"><span data-stu-id="fbd7a-117">tableid</span></span>  
    <span data-ttu-id="fbd7a-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-118">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="fbd7a-119">Cursore da cui recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-119">The cursor to retrieve data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbd7a-120">numColumnids</span><span class="sxs-lookup"><span data-stu-id="fbd7a-120">numColumnids</span></span>  
    <span data-ttu-id="fbd7a-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fbd7a-122">Numero di JET_ENUMCOLUMNIDS.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-122">The numbers of JET_ENUMCOLUMNIDS.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbd7a-123">columnIDs</span><span class="sxs-lookup"><span data-stu-id="fbd7a-123">columnids</span></span>  
    <span data-ttu-id="fbd7a-124">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="fbd7a-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="fbd7a-125">Matrice facoltativa di ID di colonna, ognuno con una matrice facoltativa di numeri itagSequence da enumerare.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-125">An optional array of column IDs, each with an optional array of itagSequence numbers to enumerate.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbd7a-126">numColumnValues</span><span class="sxs-lookup"><span data-stu-id="fbd7a-126">numColumnValues</span></span>  
    <span data-ttu-id="fbd7a-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fbd7a-128">Restituisce il numero di valori di colonna recuperati.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-128">Returns the number of column values retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbd7a-129">columnValues</span><span class="sxs-lookup"><span data-stu-id="fbd7a-129">columnValues</span></span>  
    <span data-ttu-id="fbd7a-130">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="fbd7a-130">Type: \[\]</span></span>  
    
    <span data-ttu-id="fbd7a-131">Restituisce i valori della colonna enumerata.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-131">Returns the enumerated column values.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbd7a-132">allocator</span><span class="sxs-lookup"><span data-stu-id="fbd7a-132">allocator</span></span>  
    <span data-ttu-id="fbd7a-133">Tipo: [Microsoft.ISAM.esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-133">Type: [Microsoft.Isam.Esent.Interop.JET_PFNREALLOC](./jet-pfnrealloc-delegate.md)</span></span>  
    
    <span data-ttu-id="fbd7a-134">Callback usato per allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-134">Callback used to allocate memory.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbd7a-135">allocatorContext</span><span class="sxs-lookup"><span data-stu-id="fbd7a-135">allocatorContext</span></span>  
    <span data-ttu-id="fbd7a-136">Tipo: [System. IntPtr](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-136">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="fbd7a-137">Contesto per il callback di allocazione.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-137">Context for the allocation callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbd7a-138">maxDataSize</span><span class="sxs-lookup"><span data-stu-id="fbd7a-138">maxDataSize</span></span>  
    <span data-ttu-id="fbd7a-139">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-139">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="fbd7a-140">Imposta un limite per la quantità di dati da restituire da un testo lungo o una colonna binaria di tipo Long.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-140">Sets a cap on the amount of data to return from a long text or long binary column.</span></span> <span data-ttu-id="fbd7a-141">Questo parametro può essere utilizzato per impedire l'enumerazione di un valore di colonna estremamente grande.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-141">This parameter can be used to prevent the enumeration of an extremely large column value.</span></span>

<!-- end list -->

  - <span data-ttu-id="fbd7a-142">grbit</span><span class="sxs-lookup"><span data-stu-id="fbd7a-142">grbit</span></span>  
    <span data-ttu-id="fbd7a-143">Tipo: [Microsoft. ISAM. esent. Interop. EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-143">Type: [Microsoft.Isam.Esent.Interop.EnumerateColumnsGrbit](./enumeratecolumnsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="fbd7a-144">Recupera le opzioni.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-144">Retrieve options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="fbd7a-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fbd7a-145">Return value</span></span>

<span data-ttu-id="fbd7a-146">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fbd7a-146">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="fbd7a-147">Avviso o operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="fbd7a-147">A warning or success.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fbd7a-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbd7a-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fbd7a-149">Riferimento</span><span class="sxs-lookup"><span data-stu-id="fbd7a-149">Reference</span></span>

[<span data-ttu-id="fbd7a-150">Classe API</span><span class="sxs-lookup"><span data-stu-id="fbd7a-150">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fbd7a-151">Membri API</span><span class="sxs-lookup"><span data-stu-id="fbd7a-151">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fbd7a-152">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="fbd7a-152">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
