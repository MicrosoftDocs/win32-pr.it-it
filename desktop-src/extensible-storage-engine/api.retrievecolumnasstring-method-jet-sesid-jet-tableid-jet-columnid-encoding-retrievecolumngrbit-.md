---
description: 'Altre informazioni su: metodo API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, codifica, RetrieveColumnGrbit)'
title: Metodo API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100862
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2008726577bac37e129a887af2d8b1747323c81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319798"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding-retrievecolumngrbit"></a><span data-ttu-id="c0a71-103">Metodo API. RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</span><span class="sxs-lookup"><span data-stu-id="c0a71-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="c0a71-104">Recupera un valore di colonna stringa dal record corrente.</span><span class="sxs-lookup"><span data-stu-id="c0a71-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="c0a71-105">Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</span><span class="sxs-lookup"><span data-stu-id="c0a71-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="c0a71-106">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c0a71-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c0a71-107">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c0a71-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a71-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c0a71-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding, _
    grbit As RetrieveColumnGrbit _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim grbit As RetrieveColumnGrbit
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding, grbit)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c0a71-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c0a71-109">Parameters</span></span>

  - <span data-ttu-id="c0a71-110">sesid</span><span class="sxs-lookup"><span data-stu-id="c0a71-110">sesid</span></span>  
    <span data-ttu-id="c0a71-111">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c0a71-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c0a71-112">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="c0a71-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c0a71-113">TableID</span><span class="sxs-lookup"><span data-stu-id="c0a71-113">tableid</span></span>  
    <span data-ttu-id="c0a71-114">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c0a71-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c0a71-115">Cursore da cui recuperare la colonna.</span><span class="sxs-lookup"><span data-stu-id="c0a71-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="c0a71-116">columnid</span><span class="sxs-lookup"><span data-stu-id="c0a71-116">columnid</span></span>  
    <span data-ttu-id="c0a71-117">Tipo: [Microsoft.ISAM.esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c0a71-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="c0a71-118">ColumnID da recuperare.</span><span class="sxs-lookup"><span data-stu-id="c0a71-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="c0a71-119">codifica</span><span class="sxs-lookup"><span data-stu-id="c0a71-119">encoding</span></span>  
    <span data-ttu-id="c0a71-120">Tipo: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="c0a71-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="c0a71-121">Codifica di stringhe da utilizzare per la conversione dei dati.</span><span class="sxs-lookup"><span data-stu-id="c0a71-121">The string encoding to use when converting data.</span></span>

<!-- end list -->

  - <span data-ttu-id="c0a71-122">grbit</span><span class="sxs-lookup"><span data-stu-id="c0a71-122">grbit</span></span>  
    <span data-ttu-id="c0a71-123">Tipo: [Microsoft. ISAM. esent. Interop. RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c0a71-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c0a71-124">Opzioni di recupero.</span><span class="sxs-lookup"><span data-stu-id="c0a71-124">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c0a71-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c0a71-125">Return value</span></span>

<span data-ttu-id="c0a71-126">Tipo: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c0a71-126">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="c0a71-127">Dati recuperati dalla colonna sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="c0a71-127">The data retrieved from the column as a string.</span></span> <span data-ttu-id="c0a71-128">Null se la colonna è null.</span><span class="sxs-lookup"><span data-stu-id="c0a71-128">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c0a71-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0a71-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c0a71-130">Riferimento</span><span class="sxs-lookup"><span data-stu-id="c0a71-130">Reference</span></span>

[<span data-ttu-id="c0a71-131">Classe API</span><span class="sxs-lookup"><span data-stu-id="c0a71-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c0a71-132">Membri API</span><span class="sxs-lookup"><span data-stu-id="c0a71-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c0a71-133">Overload RetrieveColumnAsString</span><span class="sxs-lookup"><span data-stu-id="c0a71-133">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="c0a71-134">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c0a71-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
