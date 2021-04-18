---
description: 'Altre informazioni su: Windows8Api. JetTryPrereadIndexRanges, metodo'
title: Metodo Windows8Api. JetTryPrereadIndexRanges (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'JetTryPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jettryprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104421
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a9664e658254de057b0e3aa8ae86813eb996a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308795"
---
# <a name="windows8apijettryprereadindexranges-method"></a><span data-ttu-id="e6f6e-103">Windows8Api. JetTryPrereadIndexRanges, metodo</span><span class="sxs-lookup"><span data-stu-id="e6f6e-103">Windows8Api.JetTryPrereadIndexRanges method</span></span>

<span data-ttu-id="e6f6e-104">Se i record con gli intervalli di chiavi specificati non sono presenti nella cache buffer, avviare le letture asincrone per inserire i record nella cache buffer del database.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-104">If the records with the specified key ranges are not in the buffer cache, then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="e6f6e-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e6f6e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="e6f6e-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e6f6e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f6e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6f6e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetTryPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbit
Dim returnValue As Boolean

returnValue = Windows8Api.JetTryPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static bool JetTryPrereadIndexRanges(
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

#### <a name="parameters"></a><span data-ttu-id="e6f6e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6f6e-108">Parameters</span></span>

  - <span data-ttu-id="e6f6e-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e6f6e-109">sesid</span></span>  
    <span data-ttu-id="e6f6e-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e6f6e-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e6f6e-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6f6e-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e6f6e-112">tableid</span></span>  
    <span data-ttu-id="e6f6e-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e6f6e-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e6f6e-114">Tabella su cui eseguire le preletture.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6f6e-115">indexRanges</span><span class="sxs-lookup"><span data-stu-id="e6f6e-115">indexRanges</span></span>  
    <span data-ttu-id="e6f6e-116">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="e6f6e-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="e6f6e-117">Intervalli di chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-117">The key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6f6e-118">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="e6f6e-118">rangeIndex</span></span>  
    <span data-ttu-id="e6f6e-119">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e6f6e-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e6f6e-120">Indice del primo intervallo di chiavi nella matrice da leggere.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-120">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6f6e-121">rangeCount</span><span class="sxs-lookup"><span data-stu-id="e6f6e-121">rangeCount</span></span>  
    <span data-ttu-id="e6f6e-122">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e6f6e-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e6f6e-123">Numero massimo di intervalli di chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-123">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6f6e-124">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="e6f6e-124">rangesPreread</span></span>  
    <span data-ttu-id="e6f6e-125">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e6f6e-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e6f6e-126">Restituisce il numero di chiavi effettivamente prelette.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-126">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6f6e-127">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="e6f6e-127">columnsPreread</span></span>  
    <span data-ttu-id="e6f6e-128">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="e6f6e-128">Type: \[\]</span></span>  
    
    <span data-ttu-id="e6f6e-129">Elenco di ID di colonna per le colonne con valore esteso da preleggere.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-129">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e6f6e-130">grbit</span><span class="sxs-lookup"><span data-stu-id="e6f6e-130">grbit</span></span>  
    <span data-ttu-id="e6f6e-131">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e6f6e-131">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e6f6e-132">Opzioni di prelettura.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-132">Preread options.</span></span> <span data-ttu-id="e6f6e-133">Utilizzato per specificare la direzione della prelettura.</span><span class="sxs-lookup"><span data-stu-id="e6f6e-133">Used to specify the direction of the preread.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e6f6e-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6f6e-134">Return value</span></span>

<span data-ttu-id="e6f6e-135">Tipo: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e6f6e-135">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e6f6e-136">**\[ true \]** se è stato eseguito un prelettura, in caso contrario **\[ false \]** .</span><span class="sxs-lookup"><span data-stu-id="e6f6e-136">**\[true\]** if some preread done, **\[false\]** otherwise.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e6f6e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6f6e-137">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e6f6e-138">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e6f6e-138">Reference</span></span>

[<span data-ttu-id="e6f6e-139">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="e6f6e-139">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="e6f6e-140">Membri di Windows8Api</span><span class="sxs-lookup"><span data-stu-id="e6f6e-140">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="e6f6e-141">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="e6f6e-141">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
