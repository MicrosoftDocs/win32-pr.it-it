---
description: 'Altre informazioni su: metodo API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Metodo API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100833
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2c29a591064c573e168903aaf83dcdd15f5b9a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319286"
---
# <a name="apiretrievecolumn-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="6618f-103">Metodo API. RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="6618f-103">Api.RetrieveColumn method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="6618f-104">Recupera un valore di colonna singola dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="6618f-104">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="6618f-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="6618f-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="6618f-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6618f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6618f-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="6618f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6618f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6618f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumn ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Byte()

returnValue = Api.RetrieveColumn(sesid, _
    tableid, columnid)
```

``` csharp
public static byte[] RetrieveColumn(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="6618f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="6618f-109">Parameters</span></span>

  - <span data-ttu-id="6618f-110">sesid</span><span class="sxs-lookup"><span data-stu-id="6618f-110">sesid</span></span>  
    <span data-ttu-id="6618f-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6618f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6618f-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="6618f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="6618f-113">TableID</span><span class="sxs-lookup"><span data-stu-id="6618f-113">tableid</span></span>  
    <span data-ttu-id="6618f-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6618f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="6618f-115">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="6618f-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="6618f-116">columnid</span><span class="sxs-lookup"><span data-stu-id="6618f-116">columnid</span></span>  
    <span data-ttu-id="6618f-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6618f-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="6618f-118">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6618f-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="6618f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6618f-119">Return value</span></span>

<span data-ttu-id="6618f-120">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="6618f-120">Type: \[\]</span></span>  
<span data-ttu-id="6618f-121">Dati recuperati dalla colonna.</span><span class="sxs-lookup"><span data-stu-id="6618f-121">The data retrieved from the column.</span></span> <span data-ttu-id="6618f-122">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="6618f-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="6618f-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6618f-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6618f-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="6618f-124">Reference</span></span>

[<span data-ttu-id="6618f-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="6618f-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6618f-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="6618f-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6618f-127">Overload RetrieveColumn</span><span class="sxs-lookup"><span data-stu-id="6618f-127">RetrieveColumn overload</span></span>](./api.retrievecolumn-method.md)

[<span data-ttu-id="6618f-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6618f-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
