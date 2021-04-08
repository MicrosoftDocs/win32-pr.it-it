---
description: 'Altre informazioni su: metodo API. JetGetSecondaryIndexBookmark'
title: API. JetGetSecondaryIndexBookmark, metodo
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0a25e78ca291271a96d06e5c0bf61c691acd4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049412"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a><span data-ttu-id="76eea-103">API. JetGetSecondaryIndexBookmark, metodo</span><span class="sxs-lookup"><span data-stu-id="76eea-103">Api.JetGetSecondaryIndexBookmark method</span></span>

<span data-ttu-id="76eea-104">Recupera un segnalibro speciale per la voce di indice secondaria in corrispondenza della posizione corrente di un cursore.</span><span class="sxs-lookup"><span data-stu-id="76eea-104">Retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="76eea-105">Questo segnalibro può quindi essere utilizzato per riposizionare in modo efficiente il cursore sulla stessa voce di indice utilizzando JetGotoSecondaryIndexBookmark.</span><span class="sxs-lookup"><span data-stu-id="76eea-105">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using JetGotoSecondaryIndexBookmark.</span></span> <span data-ttu-id="76eea-106">Questa operazione è particolarmente utile quando si riposiziona in un indice secondario che contiene chiavi duplicate o che contiene più voci di indice per lo stesso record.</span><span class="sxs-lookup"><span data-stu-id="76eea-106">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="76eea-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="76eea-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="76eea-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="76eea-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="76eea-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76eea-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="76eea-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="76eea-110">Parameters</span></span>

  - <span data-ttu-id="76eea-111">sesid</span><span class="sxs-lookup"><span data-stu-id="76eea-111">sesid</span></span>  
    <span data-ttu-id="76eea-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="76eea-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="76eea-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="76eea-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="76eea-114">TableID</span><span class="sxs-lookup"><span data-stu-id="76eea-114">tableid</span></span>  
    <span data-ttu-id="76eea-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="76eea-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="76eea-116">Cursore da cui recuperare il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="76eea-116">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="76eea-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="76eea-117">secondaryKey</span></span>  
    <span data-ttu-id="76eea-118">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="76eea-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="76eea-119">Buffer di output per la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="76eea-119">Output buffer for the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="76eea-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="76eea-120">secondaryKeySize</span></span>  
    <span data-ttu-id="76eea-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="76eea-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="76eea-122">Dimensioni del buffer della chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="76eea-122">Size of the secondary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="76eea-123">actualSecondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="76eea-123">actualSecondaryKeySize</span></span>  
    <span data-ttu-id="76eea-124">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="76eea-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="76eea-125">Restituisce la dimensione della chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="76eea-125">Returns the size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="76eea-126">primaryKey</span><span class="sxs-lookup"><span data-stu-id="76eea-126">primaryKey</span></span>  
    <span data-ttu-id="76eea-127">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="76eea-127">Type: \[\]</span></span>  
    
    <span data-ttu-id="76eea-128">Buffer di output per la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="76eea-128">Output buffer for the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="76eea-129">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="76eea-129">primaryKeySize</span></span>  
    <span data-ttu-id="76eea-130">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="76eea-130">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="76eea-131">Dimensioni del buffer di chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="76eea-131">Size of the primary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="76eea-132">actualPrimaryKeySize</span><span class="sxs-lookup"><span data-stu-id="76eea-132">actualPrimaryKeySize</span></span>  
    <span data-ttu-id="76eea-133">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="76eea-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="76eea-134">Restituisce la dimensione della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="76eea-134">Returns the size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="76eea-135">grbit</span><span class="sxs-lookup"><span data-stu-id="76eea-135">grbit</span></span>  
    <span data-ttu-id="76eea-136">Tipo: [Microsoft. ISAM. esent. Interop. GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="76eea-136">Type: [Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="76eea-137">Opzioni per la chiamata.</span><span class="sxs-lookup"><span data-stu-id="76eea-137">Options for the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="76eea-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="76eea-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="76eea-139">Riferimento</span><span class="sxs-lookup"><span data-stu-id="76eea-139">Reference</span></span>

[<span data-ttu-id="76eea-140">Classe API</span><span class="sxs-lookup"><span data-stu-id="76eea-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="76eea-141">Membri API</span><span class="sxs-lookup"><span data-stu-id="76eea-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="76eea-142">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="76eea-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
