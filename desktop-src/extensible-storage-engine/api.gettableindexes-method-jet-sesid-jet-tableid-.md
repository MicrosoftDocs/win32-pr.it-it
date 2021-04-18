---
description: 'Altre informazioni su: metodo API. GetTableIndexes (JET_SESID, JET_TABLEID)'
title: Metodo API. GetTableIndexes (JET_SESID, JET_TABLEID)
TOCTitle: GetTableIndexes method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55107219
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8708f285445b13ecb1c9d2cb306ec14c7976905b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306324"
---
# <a name="apigettableindexes-method-jet_sesid-jet_tableid"></a><span data-ttu-id="969e7-103">Metodo API. GetTableIndexes (JET_SESID, JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="969e7-103">Api.GetTableIndexes method (JET_SESID, JET_TABLEID)</span></span>

<span data-ttu-id="969e7-104">Scorre tutti gli indici della tabella, restituendo le informazioni su ognuna di esse.</span><span class="sxs-lookup"><span data-stu-id="969e7-104">Iterates over all the indexes in the table, returning information about each one.</span></span>

<span data-ttu-id="969e7-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="969e7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="969e7-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="969e7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="969e7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="969e7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="969e7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="969e7-108">Parameters</span></span>

  - <span data-ttu-id="969e7-109">sesid</span><span class="sxs-lookup"><span data-stu-id="969e7-109">sesid</span></span>  
    <span data-ttu-id="969e7-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="969e7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="969e7-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="969e7-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="969e7-112">TableID</span><span class="sxs-lookup"><span data-stu-id="969e7-112">tableid</span></span>  
    <span data-ttu-id="969e7-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="969e7-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="969e7-114">Tabella per cui recuperare le informazioni sugli indici.</span><span class="sxs-lookup"><span data-stu-id="969e7-114">The table to retrieve index information for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="969e7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="969e7-115">Return value</span></span>

<span data-ttu-id="969e7-116">Tipo: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span><span class="sxs-lookup"><span data-stu-id="969e7-116">Type: [System.Collections.Generic.IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\></span></span>  
<span data-ttu-id="969e7-117">Iteratore su un IndexInfo per ogni indice nella tabella.</span><span class="sxs-lookup"><span data-stu-id="969e7-117">An iterator over an IndexInfo for each index in the table.</span></span>  

## <a name="see-also"></a><span data-ttu-id="969e7-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="969e7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="969e7-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="969e7-119">Reference</span></span>

[<span data-ttu-id="969e7-120">Classe API</span><span class="sxs-lookup"><span data-stu-id="969e7-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="969e7-121">Membri API</span><span class="sxs-lookup"><span data-stu-id="969e7-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="969e7-122">Overload GetTableIndexes</span><span class="sxs-lookup"><span data-stu-id="969e7-122">GetTableIndexes overload</span></span>](./api.gettableindexes-method.md)

[<span data-ttu-id="969e7-123">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="969e7-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
