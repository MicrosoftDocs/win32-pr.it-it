---
description: 'Altre informazioni su: Windows8Api. JetPrereadIndexRanges, metodo'
title: Metodo Windows8Api. JetPrereadIndexRanges (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104451
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetPrereadIndexRanges
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 986213a054dec54e92e4ecfe6fb0abd541b451ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308798"
---
# <a name="windows8apijetprereadindexranges-method"></a><span data-ttu-id="178e5-103">Windows8Api. JetPrereadIndexRanges, metodo</span><span class="sxs-lookup"><span data-stu-id="178e5-103">Windows8Api.JetPrereadIndexRanges method</span></span>

<span data-ttu-id="178e5-104">Se i record con gli intervalli di chiavi specificati non sono presenti nella cache buffer, avviare le letture asincrone per inserire i record nella cache buffer del database.</span><span class="sxs-lookup"><span data-stu-id="178e5-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="178e5-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="178e5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="178e5-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="178e5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="178e5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="178e5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.JetPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static void JetPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="178e5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="178e5-108">Parameters</span></span>

  - <span data-ttu-id="178e5-109">sesid</span><span class="sxs-lookup"><span data-stu-id="178e5-109">sesid</span></span>  
    <span data-ttu-id="178e5-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="178e5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="178e5-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="178e5-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="178e5-112">TableID</span><span class="sxs-lookup"><span data-stu-id="178e5-112">tableid</span></span>  
    <span data-ttu-id="178e5-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="178e5-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="178e5-114">Tabella su cui eseguire le preletture.</span><span class="sxs-lookup"><span data-stu-id="178e5-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="178e5-115">indexRanges</span><span class="sxs-lookup"><span data-stu-id="178e5-115">indexRanges</span></span>  
    <span data-ttu-id="178e5-116">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="178e5-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="178e5-117">Intervalli di chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="178e5-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="178e5-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="178e5-118">rangeIndex</span></span>  
    <span data-ttu-id="178e5-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="178e5-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="178e5-120">Indice del primo intervallo di chiavi nella matrice da leggere.</span><span class="sxs-lookup"><span data-stu-id="178e5-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="178e5-121">rangeCount</span><span class="sxs-lookup"><span data-stu-id="178e5-121">rangeCount</span></span>  
    <span data-ttu-id="178e5-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="178e5-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="178e5-123">Numero massimo di intervalli di chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="178e5-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="178e5-124">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="178e5-124">rangesPreread</span></span>  
    <span data-ttu-id="178e5-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="178e5-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="178e5-126">Restituisce il numero di chiavi effettivamente prelette.</span><span class="sxs-lookup"><span data-stu-id="178e5-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="178e5-127">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="178e5-127">columnsPreread</span></span>  
    <span data-ttu-id="178e5-128">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="178e5-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="178e5-129">Elenco di ID di colonna per le colonne con valore esteso da preleggere.</span><span class="sxs-lookup"><span data-stu-id="178e5-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="178e5-130">grbit</span><span class="sxs-lookup"><span data-stu-id="178e5-130">grbit</span></span>  
    <span data-ttu-id="178e5-131">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="178e5-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="178e5-132">Opzioni di prelettura.</span><span class="sxs-lookup"><span data-stu-id="178e5-132">Preread options.</span></span> <span data-ttu-id="178e5-133">Utilizzato per specificare la direzione della prelettura.</span><span class="sxs-lookup"><span data-stu-id="178e5-133">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="178e5-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="178e5-134">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="178e5-135">Riferimento</span><span class="sxs-lookup"><span data-stu-id="178e5-135">Reference</span></span>

[<span data-ttu-id="178e5-136">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="178e5-136">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="178e5-137">Membri di Windows8Api</span><span class="sxs-lookup"><span data-stu-id="178e5-137">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="178e5-138">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="178e5-138">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
