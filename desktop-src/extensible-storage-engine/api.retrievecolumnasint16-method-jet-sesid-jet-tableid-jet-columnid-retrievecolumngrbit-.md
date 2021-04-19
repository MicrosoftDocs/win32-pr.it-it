---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Metodo API. RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt16(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint16(v=EXCHG.10)
ms:contentKeyID: 55100890
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt16
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1972d3cc8ac75d25b140f00e6ff215c7d1a47106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317532"
---
# <a name="apiretrievecolumnasint16-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="a7c1c-103">Metodo API. RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="a7c1c-103">Api.RetrieveColumnAsInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="a7c1c-104">Recupera un valore di colonna Int16 dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="a7c1c-104">Retrieves an int16 column value from the current record.</span></span> <span data-ttu-id="a7c1c-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="a7c1c-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="a7c1c-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a7c1c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a7c1c-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a7c1c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c1c-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7c1c-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt16 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Short)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Short)

returnValue = Api.RetrieveColumnAsInt16(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<short> RetrieveColumnAsInt16(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="a7c1c-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7c1c-109">Parameters</span></span>

  - <span data-ttu-id="a7c1c-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a7c1c-110">sesid</span></span>  
    <span data-ttu-id="a7c1c-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a7c1c-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a7c1c-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="a7c1c-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7c1c-113">TableID</span><span class="sxs-lookup"><span data-stu-id="a7c1c-113">tableid</span></span>  
    <span data-ttu-id="a7c1c-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a7c1c-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a7c1c-115">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="a7c1c-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7c1c-116">columnid</span><span class="sxs-lookup"><span data-stu-id="a7c1c-116">columnid</span></span>  
    <span data-ttu-id="a7c1c-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a7c1c-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="a7c1c-118">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="a7c1c-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="a7c1c-119">grbit</span><span class="sxs-lookup"><span data-stu-id="a7c1c-119">grbit</span></span>  
    <span data-ttu-id="a7c1c-120">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a7c1c-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a7c1c-121">Opzioni di recupero.</span><span class="sxs-lookup"><span data-stu-id="a7c1c-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a7c1c-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a7c1c-122">Return value</span></span>

<span data-ttu-id="a7c1c-123">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int16](/dotnet/api/system.int16)\></span><span class="sxs-lookup"><span data-stu-id="a7c1c-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int16](/dotnet/api/system.int16)\></span></span>  
<span data-ttu-id="a7c1c-124">Dati recuperati dalla colonna come short.</span><span class="sxs-lookup"><span data-stu-id="a7c1c-124">The data retrieved from the column as a short.</span></span> <span data-ttu-id="a7c1c-125">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="a7c1c-125">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a7c1c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7c1c-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a7c1c-127">Riferimento</span><span class="sxs-lookup"><span data-stu-id="a7c1c-127">Reference</span></span>

[<span data-ttu-id="a7c1c-128">Classe API</span><span class="sxs-lookup"><span data-stu-id="a7c1c-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a7c1c-129">Membri API</span><span class="sxs-lookup"><span data-stu-id="a7c1c-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a7c1c-130">Overload RetrieveColumnAsInt16</span><span class="sxs-lookup"><span data-stu-id="a7c1c-130">RetrieveColumnAsInt16 overload</span></span>](./api.retrievecolumnasint16-method.md)

[<span data-ttu-id="a7c1c-131">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="a7c1c-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
