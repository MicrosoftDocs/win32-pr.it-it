---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)'
title: Metodo API. RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)
TOCTitle: RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasuint16(v=EXCHG.10)
ms:contentKeyID: 55100861
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsUInt16
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8a89ed851d54d142d5a8253fe94707848b6df7de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233239"
---
# <a name="apiretrievecolumnasuint16-method-jet_sesid-jet_tableid-jet_columnid"></a><span data-ttu-id="88688-103">Metodo API. RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="88688-103">Api.RetrieveColumnAsUInt16 method (JET_SESID, JET_TABLEID, JET_COLUMNID)</span></span>

<span data-ttu-id="88688-104">Recupera un valore di colonna UInt16 dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="88688-104">Retrieves a uint16 column value from the current record.</span></span> <span data-ttu-id="88688-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="88688-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="88688-106">Questa API non è conforme a CLS.</span><span class="sxs-lookup"><span data-stu-id="88688-106">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="88688-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="88688-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="88688-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="88688-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="88688-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88688-109">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function RetrieveColumnAsUInt16 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID _
) As Nullable(Of UShort)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim returnValue As Nullable(Of UShort)

returnValue = Api.RetrieveColumnAsUInt16(sesid, _
    tableid, columnid)
```

``` csharp
[CLSCompliantAttribute(false)]
public static Nullable<ushort> RetrieveColumnAsUInt16(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid
)
```

#### <a name="parameters"></a><span data-ttu-id="88688-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="88688-110">Parameters</span></span>

  - <span data-ttu-id="88688-111">sesid</span><span class="sxs-lookup"><span data-stu-id="88688-111">sesid</span></span>  
    <span data-ttu-id="88688-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="88688-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="88688-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="88688-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="88688-114">TableID</span><span class="sxs-lookup"><span data-stu-id="88688-114">tableid</span></span>  
    <span data-ttu-id="88688-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="88688-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="88688-116">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="88688-116">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="88688-117">columnid</span><span class="sxs-lookup"><span data-stu-id="88688-117">columnid</span></span>  
    <span data-ttu-id="88688-118">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="88688-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="88688-119">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="88688-119">The columnid to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="88688-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88688-120">Return value</span></span>

<span data-ttu-id="88688-121">Tipo: [System. Nullable](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span><span class="sxs-lookup"><span data-stu-id="88688-121">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[UInt16](/dotnet/api/system.uint16)\></span></span>  
<span data-ttu-id="88688-122">Dati recuperati dalla colonna come oggetto UInt16.</span><span class="sxs-lookup"><span data-stu-id="88688-122">The data retrieved from the column as an UInt16.</span></span> <span data-ttu-id="88688-123">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="88688-123">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="88688-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88688-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="88688-125">Riferimento</span><span class="sxs-lookup"><span data-stu-id="88688-125">Reference</span></span>

[<span data-ttu-id="88688-126">Classe API</span><span class="sxs-lookup"><span data-stu-id="88688-126">Api class</span></span>](./api-class.md)

[<span data-ttu-id="88688-127">Membri API</span><span class="sxs-lookup"><span data-stu-id="88688-127">Api members</span></span>](./api-members.md)

[<span data-ttu-id="88688-128">Overload RetrieveColumnAsUInt16</span><span class="sxs-lookup"><span data-stu-id="88688-128">RetrieveColumnAsUInt16 overload</span></span>](./api.retrievecolumnasuint16-method.md)

[<span data-ttu-id="88688-129">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="88688-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
