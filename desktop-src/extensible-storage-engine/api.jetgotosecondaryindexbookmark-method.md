---
description: 'Altre informazioni su: metodo API. JetGotoSecondaryIndexBookmark'
title: API. JetGotoSecondaryIndexBookmark, metodo
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af146236a2a5398dfb0b7b81f42dcfc6227a6de9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318835"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a><span data-ttu-id="f7a41-103">API. JetGotoSecondaryIndexBookmark, metodo</span><span class="sxs-lookup"><span data-stu-id="f7a41-103">Api.JetGotoSecondaryIndexBookmark method</span></span>

<span data-ttu-id="f7a41-104">Posiziona un cursore in una voce di indice associata al segnalibro dell'indice secondario specificato.</span><span class="sxs-lookup"><span data-stu-id="f7a41-104">Positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="f7a41-105">Il segnalibro dell'indice secondario deve essere usato con lo stesso indice nella stessa tabella da cui è stato originariamente recuperato.</span><span class="sxs-lookup"><span data-stu-id="f7a41-105">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="f7a41-106">Il segnalibro dell'indice secondario per una voce di indice può essere recuperato tramite JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, GotoSecondaryIndexBookmarkGrbit).</span><span class="sxs-lookup"><span data-stu-id="f7a41-106">The secondary index bookmark for an index entry can be retrieved using JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit).</span></span>

<span data-ttu-id="f7a41-107">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f7a41-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f7a41-108">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f7a41-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f7a41-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f7a41-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f7a41-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f7a41-110">Parameters</span></span>

  - <span data-ttu-id="f7a41-111">sesid</span><span class="sxs-lookup"><span data-stu-id="f7a41-111">sesid</span></span>  
    <span data-ttu-id="f7a41-112">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f7a41-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="f7a41-113">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="f7a41-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7a41-114">TableID</span><span class="sxs-lookup"><span data-stu-id="f7a41-114">tableid</span></span>  
    <span data-ttu-id="f7a41-115">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f7a41-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="f7a41-116">Cursore della tabella da posizionare.</span><span class="sxs-lookup"><span data-stu-id="f7a41-116">The table cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7a41-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="f7a41-117">secondaryKey</span></span>  
    <span data-ttu-id="f7a41-118">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="f7a41-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="f7a41-119">Buffer contenente la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="f7a41-119">The buffer that contains the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7a41-120">secondaryKeySize</span><span class="sxs-lookup"><span data-stu-id="f7a41-120">secondaryKeySize</span></span>  
    <span data-ttu-id="f7a41-121">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f7a41-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f7a41-122">Dimensione della chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="f7a41-122">The size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7a41-123">primaryKey</span><span class="sxs-lookup"><span data-stu-id="f7a41-123">primaryKey</span></span>  
    <span data-ttu-id="f7a41-124">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="f7a41-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="f7a41-125">Buffer contenente la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="f7a41-125">The buffer that contains the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7a41-126">primaryKeySize</span><span class="sxs-lookup"><span data-stu-id="f7a41-126">primaryKeySize</span></span>  
    <span data-ttu-id="f7a41-127">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f7a41-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="f7a41-128">Dimensione della chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="f7a41-128">The size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="f7a41-129">grbit</span><span class="sxs-lookup"><span data-stu-id="f7a41-129">grbit</span></span>  
    <span data-ttu-id="f7a41-130">Tipo: [Microsoft. ISAM. esent. Interop. GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f7a41-130">Type: [Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f7a41-131">Opzioni per posizionare il segnalibro.</span><span class="sxs-lookup"><span data-stu-id="f7a41-131">Options for positioning the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7a41-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f7a41-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f7a41-133">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f7a41-133">Reference</span></span>

[<span data-ttu-id="f7a41-134">Classe API</span><span class="sxs-lookup"><span data-stu-id="f7a41-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="f7a41-135">Membri API</span><span class="sxs-lookup"><span data-stu-id="f7a41-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="f7a41-136">Spazio dei nomi Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="f7a41-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
