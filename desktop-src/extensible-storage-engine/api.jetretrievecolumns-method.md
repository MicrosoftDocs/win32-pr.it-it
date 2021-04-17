---
description: 'Altre informazioni su: metodo API. JetRetrieveColumns'
title: API. JetRetrieveColumns, metodo
TOCTitle: 'JetRetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100797
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3fd4db2ce8cbcad5f74db7d4c95363aa68e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306269"
---
# <a name="apijetretrievecolumns-method"></a><span data-ttu-id="7389a-103">API. JetRetrieveColumns, metodo</span><span class="sxs-lookup"><span data-stu-id="7389a-103">Api.JetRetrieveColumns method</span></span>

<span data-ttu-id="7389a-104">Recupera più valori di colonna dal record corrente in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="7389a-104">Retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="7389a-105">Una matrice di strutture di JET_RETRIEVECOLUMN viene utilizzata per descrivere il set di valori di colonna da recuperare e per descrivere i buffer di output per ogni valore di colonna da recuperare.</span><span class="sxs-lookup"><span data-stu-id="7389a-105">An array of JET_RETRIEVECOLUMN structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

<span data-ttu-id="7389a-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7389a-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7389a-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7389a-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7389a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7389a-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    retrievecolumns As JET_RETRIEVECOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim retrievecolumns As JET_RETRIEVECOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumns(sesid, _
    tableid, retrievecolumns, numColumns)
```

``` csharp
public static JET_wrn JetRetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RETRIEVECOLUMN[] retrievecolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="7389a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7389a-109">Parameters</span></span>

  - <span data-ttu-id="7389a-110">sesid</span><span class="sxs-lookup"><span data-stu-id="7389a-110">sesid</span></span>  
    <span data-ttu-id="7389a-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7389a-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7389a-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="7389a-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7389a-113">TableID</span><span class="sxs-lookup"><span data-stu-id="7389a-113">tableid</span></span>  
    <span data-ttu-id="7389a-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7389a-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7389a-115">Cursore da cui recuperare i dati.</span><span class="sxs-lookup"><span data-stu-id="7389a-115">The cursor to retrieve the data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="7389a-116">retrievecolumns</span><span class="sxs-lookup"><span data-stu-id="7389a-116">retrievecolumns</span></span>  
    <span data-ttu-id="7389a-117">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="7389a-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="7389a-118">Matrice di uno o più [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) oggetti che descrivono i dati da recuperare.</span><span class="sxs-lookup"><span data-stu-id="7389a-118">An array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) objects describing the data to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="7389a-119">numColumns</span><span class="sxs-lookup"><span data-stu-id="7389a-119">numColumns</span></span>  
    <span data-ttu-id="7389a-120">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7389a-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7389a-121">Numero di voci nella matrice di colonne.</span><span class="sxs-lookup"><span data-stu-id="7389a-121">The number of entries in the columns array.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7389a-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7389a-122">Return value</span></span>

<span data-ttu-id="7389a-123">Tipo: [Microsoft.ISAM.esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7389a-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="7389a-124">Se una colonna recuperata viene troncata a causa di un buffer di lunghezza insufficiente, l'API restituirà [BufferTruncated](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="7389a-124">If any column retrieved is truncated due to an insufficient length buffer, then the API will return [BufferTruncated](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="7389a-125">Tuttavia, altri errori JET_wrnColumnNull vengono restituiti solo nel campo di errore dell'oggetto [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7389a-125">However other errors JET_wrnColumnNull are returned only in the error field of the [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) object.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7389a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7389a-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7389a-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="7389a-127">Reference</span></span>

[<span data-ttu-id="7389a-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="7389a-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7389a-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="7389a-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7389a-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="7389a-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
