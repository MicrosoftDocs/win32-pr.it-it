---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)'
title: Metodo API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasint32(v=EXCHG.10)
ms:contentKeyID: 55100859
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsInt32
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e9f963d298610fb36f6b1f9c9ff3a0bfbfa2501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524738"
---
# <a name="apiretrievecolumnasint32-method-jet_sesid-jet_tableid-jet_columnid-retrievecolumngrbit"></a><span data-ttu-id="ffabb-103">Metodo API. RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="ffabb-103">Api.RetrieveColumnAsInt32 method (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="ffabb-104">Recupera un valore di colonna Int32 dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="ffabb-104">Retrieves an int32 column value from the current record.</span></span> <span data-ttu-id="ffabb-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="ffabb-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="ffabb-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ffabb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ffabb-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ffabb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ffabb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffabb-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsInt32 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    grbit As RetrieveColumnGrbit _
) As Nullable(Of Integer)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim grbit As RetrieveColumnGrbit
Dim returnValue As Nullable(Of Integer)

returnValue = Api.RetrieveColumnAsInt32(sesid, _
    tableid, columnid, grbit)
```

``` csharp
public static Nullable<int> RetrieveColumnAsInt32(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="ffabb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffabb-109">Parameters</span></span>

  - <span data-ttu-id="ffabb-110">sesid</span><span class="sxs-lookup"><span data-stu-id="ffabb-110">sesid</span></span>  
    <span data-ttu-id="ffabb-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ffabb-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ffabb-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ffabb-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ffabb-113">TableID</span><span class="sxs-lookup"><span data-stu-id="ffabb-113">tableid</span></span>  
    <span data-ttu-id="ffabb-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ffabb-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ffabb-115">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="ffabb-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="ffabb-116">columnid</span><span class="sxs-lookup"><span data-stu-id="ffabb-116">columnid</span></span>  
    <span data-ttu-id="ffabb-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ffabb-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ffabb-118">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="ffabb-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="ffabb-119">grbit</span><span class="sxs-lookup"><span data-stu-id="ffabb-119">grbit</span></span>  
    <span data-ttu-id="ffabb-120">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="ffabb-120">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="ffabb-121">Opzioni di recupero.</span><span class="sxs-lookup"><span data-stu-id="ffabb-121">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ffabb-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffabb-122">Return value</span></span>

<span data-ttu-id="ffabb-123">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span><span class="sxs-lookup"><span data-stu-id="ffabb-123">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Int32](/dotnet/api/system.int32)\></span></span>  
<span data-ttu-id="ffabb-124">Dati recuperati dalla colonna come int. Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="ffabb-124">The data retrieved from the column as an int. Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ffabb-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffabb-125">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ffabb-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="ffabb-126">Reference</span></span>

[<span data-ttu-id="ffabb-127">Classe API</span><span class="sxs-lookup"><span data-stu-id="ffabb-127">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ffabb-128">Membri API</span><span class="sxs-lookup"><span data-stu-id="ffabb-128">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ffabb-129">Overload RetrieveColumnAsInt32</span><span class="sxs-lookup"><span data-stu-id="ffabb-129">RetrieveColumnAsInt32 overload</span></span>](./api.retrievecolumnasint32-method.md)

[<span data-ttu-id="ffabb-130">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ffabb-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
