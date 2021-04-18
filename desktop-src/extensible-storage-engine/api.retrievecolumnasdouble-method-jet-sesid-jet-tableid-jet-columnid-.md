---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Metodo API. RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsDouble method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDouble(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdouble(v=EXCHG.10)
ms:contentKeyID: 55100847
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDouble
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a9bf86595870b03447dd8a859ac66f0aa0c5f9a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314091"
---
# <a name="apiretrievecolumnasdouble-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="60795-103">Metodo API. RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="60795-103">Api.RetrieveColumnAsDouble method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="60795-104">Recupera un valore di colonna doppia dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="60795-104">Retrieves a double column value from the current record.</span></span> <span data-ttu-id="60795-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="60795-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="60795-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="60795-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="60795-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="60795-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="60795-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60795-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDouble ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of Double)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of Double)

returnValue = Api.RetrieveColumnAsDouble(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<double> RetrieveColumnAsDouble(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="60795-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="60795-109">Parameters</span></span>

  - <span data-ttu-id="60795-110">sesid</span><span class="sxs-lookup"><span data-stu-id="60795-110">sesid</span></span>  
    <span data-ttu-id="60795-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="60795-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="60795-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="60795-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="60795-113">TableID</span><span class="sxs-lookup"><span data-stu-id="60795-113">tableid</span></span>  
    <span data-ttu-id="60795-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="60795-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="60795-115">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="60795-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="60795-116">columnid</span><span class="sxs-lookup"><span data-stu-id="60795-116">columnid</span></span>  
    <span data-ttu-id="60795-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="60795-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="60795-118">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="60795-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="60795-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60795-119">Return value</span></span>

<span data-ttu-id="60795-120">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[Double](/dotnet/api/system.double)\></span><span class="sxs-lookup"><span data-stu-id="60795-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[Double](/dotnet/api/system.double)\></span></span>  
<span data-ttu-id="60795-121">Dati recuperati dalla colonna come Double.</span><span class="sxs-lookup"><span data-stu-id="60795-121">The data retrieved from the column as a double.</span></span> <span data-ttu-id="60795-122">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="60795-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="60795-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60795-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="60795-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="60795-124">Reference</span></span>

[<span data-ttu-id="60795-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="60795-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="60795-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="60795-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="60795-127">Overload RetrieveColumnAsDouble</span><span class="sxs-lookup"><span data-stu-id="60795-127">RetrieveColumnAsDouble overload</span></span>](./api.retrievecolumnasdouble-method.md)

[<span data-ttu-id="60795-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="60795-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
