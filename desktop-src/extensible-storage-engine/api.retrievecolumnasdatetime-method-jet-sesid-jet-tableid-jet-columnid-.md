---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Metodo API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasdatetime(v=EXCHG.10)
ms:contentKeyID: 55100870
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsDateTime
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7176fa1c78b9910b68d0b3c9e7ce4f7e46519020
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305558"
---
# <a name="apiretrievecolumnasdatetime-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="62e7e-103">Metodo API. RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="62e7e-103">Api.RetrieveColumnAsDateTime method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="62e7e-104">Recupera un valore di colonna DateTime dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="62e7e-104">Retrieves a datetime column value from the current record.</span></span> <span data-ttu-id="62e7e-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="62e7e-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="62e7e-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="62e7e-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="62e7e-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="62e7e-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="62e7e-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62e7e-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsDateTime ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of DateTime)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of DateTime)

returnValue = Api.RetrieveColumnAsDateTime(sesid, _
    tableid, columnid)
```

``` csharp
public static Nullable<DateTime> RetrieveColumnAsDateTime(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="62e7e-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="62e7e-109">Parameters</span></span>

  - <span data-ttu-id="62e7e-110">sesid</span><span class="sxs-lookup"><span data-stu-id="62e7e-110">sesid</span></span>  
    <span data-ttu-id="62e7e-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="62e7e-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="62e7e-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="62e7e-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="62e7e-113">TableID</span><span class="sxs-lookup"><span data-stu-id="62e7e-113">tableid</span></span>  
    <span data-ttu-id="62e7e-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="62e7e-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="62e7e-115">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="62e7e-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="62e7e-116">columnid</span><span class="sxs-lookup"><span data-stu-id="62e7e-116">columnid</span></span>  
    <span data-ttu-id="62e7e-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="62e7e-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="62e7e-118">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="62e7e-118">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="62e7e-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62e7e-119">Return value</span></span>

<span data-ttu-id="62e7e-120">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="62e7e-120">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="62e7e-121">Dati recuperati dalla colonna come valore DateTime.</span><span class="sxs-lookup"><span data-stu-id="62e7e-121">The data retrieved from the column as a datetime.</span></span> <span data-ttu-id="62e7e-122">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="62e7e-122">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="62e7e-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62e7e-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="62e7e-124">Riferimento</span><span class="sxs-lookup"><span data-stu-id="62e7e-124">Reference</span></span>

[<span data-ttu-id="62e7e-125">Classe API</span><span class="sxs-lookup"><span data-stu-id="62e7e-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="62e7e-126">Membri API</span><span class="sxs-lookup"><span data-stu-id="62e7e-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="62e7e-127">Overload RetrieveColumnAsDateTime</span><span class="sxs-lookup"><span data-stu-id="62e7e-127">RetrieveColumnAsDateTime overload</span></span>](./api.retrievecolumnasdatetime-method.md)

[<span data-ttu-id="62e7e-128">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="62e7e-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
