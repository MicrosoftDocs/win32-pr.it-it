---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Metodo API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint64(v=EXCHG.10)
ms:contentKeyID: 55100864
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt64
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ef62c1faa4a7060996d587a92838bdced560350
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316958"
---
# <a name="apiretrievecolumnasuint64-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="1d9bc-103">Metodo API. RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="1d9bc-103">Api.RetrieveColumnAsUInt64 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="1d9bc-104">Recupera un valore di colonna UInt64 dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-104">Retrieves a uint64 column value from the current record.</span></span> <span data-ttu-id="1d9bc-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="1d9bc-106">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="1d9bc-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1d9bc-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1d9bc-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1d9bc-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9bc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d9bc-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt64 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of ULong)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of ULong)

returnValue = Api.RetrieveColumnAsUInt64(sesid, _
    tableid, columnid)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ulong> RetrieveColumnAsUInt64(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="1d9bc-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d9bc-110">Parameters</span></span>

  - <span data-ttu-id="1d9bc-111">sesid</span><span class="sxs-lookup"><span data-stu-id="1d9bc-111">sesid</span></span>  
    <span data-ttu-id="1d9bc-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d9bc-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1d9bc-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d9bc-114">TableID</span><span class="sxs-lookup"><span data-stu-id="1d9bc-114">tableid</span></span>  
    <span data-ttu-id="1d9bc-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d9bc-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1d9bc-116">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="1d9bc-117">columnid</span><span class="sxs-lookup"><span data-stu-id="1d9bc-117">columnid</span></span>  
    <span data-ttu-id="1d9bc-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1d9bc-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="1d9bc-119">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1d9bc-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d9bc-120">Return value</span></span>

<span data-ttu-id="1d9bc-121">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span><span class="sxs-lookup"><span data-stu-id="1d9bc-121">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt64](/dotnet/api/system.uint64)\></span></span>  
<span data-ttu-id="1d9bc-122">Dati recuperati dalla colonna come UInt64.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-122">The data retrieved from the column as an UInt64.</span></span> <span data-ttu-id="1d9bc-123">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="1d9bc-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1d9bc-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d9bc-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1d9bc-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="1d9bc-125">Reference</span></span>

[<span data-ttu-id="1d9bc-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="1d9bc-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1d9bc-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="1d9bc-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1d9bc-128">Overload RetrieveColumnAsUInt64</span><span class="sxs-lookup"><span data-stu-id="1d9bc-128">RetrieveColumnAsUInt64 overload</span></span>](./api.retrievecolumnasuint64-method.md)

[<span data-ttu-id="1d9bc-129">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="1d9bc-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
