---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Metodo API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdatetime(v=EXCHG.10)
ms:contentKeyID: 55100843
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: befd4e7256c9d1ca52d6f0239f5e56c21842a85d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318817"
---
# <a name="apiretrievecolumnasdatetime-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="64f0e-103">Metodo API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="64f0e-103">Api.RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="64f0e-104">Recupera un valore di colonna DateTime dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="64f0e-104">Retrieves a datetime column value from the current record.</span></span> <span data-ttu-id="64f0e-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="64f0e-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="64f0e-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="64f0e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="64f0e-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="64f0e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="64f0e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64f0e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDateTime ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of DateTime)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of DateTime)

returnValue = Api.RetrieveColumnAsDateTime(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<DateTime> RetrieveColumnAsDateTime(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="64f0e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="64f0e-109">Parameters</span></span>

  - <span data-ttu-id="64f0e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="64f0e-110">sesid</span></span>  
    <span data-ttu-id="64f0e-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="64f0e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="64f0e-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="64f0e-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="64f0e-113">TableID</span><span class="sxs-lookup"><span data-stu-id="64f0e-113">tableid</span></span>  
    <span data-ttu-id="64f0e-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="64f0e-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="64f0e-115">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="64f0e-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="64f0e-116">columnid</span><span class="sxs-lookup"><span data-stu-id="64f0e-116">columnid</span></span>  
    <span data-ttu-id="64f0e-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="64f0e-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="64f0e-118">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="64f0e-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="64f0e-119">grbit</span><span class="sxs-lookup"><span data-stu-id="64f0e-119">grbit</span></span>  
    <span data-ttu-id="64f0e-120">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="64f0e-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="64f0e-121">Opzioni di recupero.</span><span class="sxs-lookup"><span data-stu-id="64f0e-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="64f0e-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64f0e-122">Return value</span></span>

<span data-ttu-id="64f0e-123">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="64f0e-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="64f0e-124">Dati recuperati dalla colonna come valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="64f0e-124">The data retrieved from the column as a datetime.</span></span> <span data-ttu-id="64f0e-125">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="64f0e-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="64f0e-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64f0e-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="64f0e-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="64f0e-127">Reference</span></span>

[<span data-ttu-id="64f0e-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="64f0e-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="64f0e-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="64f0e-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="64f0e-130">Overload RetrieveColumnAsDateTime</span><span class="sxs-lookup"><span data-stu-id="64f0e-130">RetrieveColumnAsDateTime overload</span></span>](./api.retrievecolumnasdatetime-method.md)

[<span data-ttu-id="64f0e-131">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="64f0e-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
