---
description: 'Altre informazioni su: Windows8Api. PrereadKeyRanges, metodo'
title: Metodo Windows8Api. PrereadKeyRanges (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 091c1f92512fd9a55bb4acd4d824567acc19fdde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966949"
---
# <a name="windows8apiprereadkeyranges-method"></a><span data-ttu-id="e87ea-103">Windows8Api. PrereadKeyRanges, metodo</span><span class="sxs-lookup"><span data-stu-id="e87ea-103">Windows8Api.PrereadKeyRanges method</span></span>

<span data-ttu-id="e87ea-104">Se i record con gli intervalli di chiavi specificati non sono presenti nella cache buffer, avviare le letture asincrone per inserire i record nella cache buffer del database.</span><span class="sxs-lookup"><span data-stu-id="e87ea-104">If the records with the specified key ranges are not in the buffer cache then start asynchronous reads to bring the records into the database buffer cache.</span></span>

<span data-ttu-id="e87ea-105">**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e87ea-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="e87ea-106">**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e87ea-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e87ea-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e87ea-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e87ea-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e87ea-108">Parameters</span></span>

  - <span data-ttu-id="e87ea-109">sesid</span><span class="sxs-lookup"><span data-stu-id="e87ea-109">sesid</span></span>  
    <span data-ttu-id="e87ea-110">Tipo: [Microsoft.ISAM.esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e87ea-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e87ea-111">Sessione da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="e87ea-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e87ea-112">tableid</span></span>  
    <span data-ttu-id="e87ea-113">Tipo: [Microsoft.ISAM.esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e87ea-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e87ea-114">Tabella su cui eseguire le preletture.</span><span class="sxs-lookup"><span data-stu-id="e87ea-114">The table to issue the prereads against.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-115">keysStart</span><span class="sxs-lookup"><span data-stu-id="e87ea-115">keysStart</span></span>  
    <span data-ttu-id="e87ea-116">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="e87ea-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="e87ea-117">Inizio degli intervalli di chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="e87ea-117">The start of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-118">keyStartLengths</span><span class="sxs-lookup"><span data-stu-id="e87ea-118">keyStartLengths</span></span>  
    <span data-ttu-id="e87ea-119">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="e87ea-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="e87ea-120">Lunghezza dei tasti di inizio per la prelettura.</span><span class="sxs-lookup"><span data-stu-id="e87ea-120">The lengths of the start keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-121">Invio di un invio</span><span class="sxs-lookup"><span data-stu-id="e87ea-121">keysEnd</span></span>  
    <span data-ttu-id="e87ea-122">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="e87ea-122">Type: \[\]</span></span>  
    
    <span data-ttu-id="e87ea-123">Fine dell'intervallo di chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="e87ea-123">The end of key rangess to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-124">keyEndLengths</span><span class="sxs-lookup"><span data-stu-id="e87ea-124">keyEndLengths</span></span>  
    <span data-ttu-id="e87ea-125">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="e87ea-125">Type: \[\]</span></span>  
    
    <span data-ttu-id="e87ea-126">Lunghezza dei tasti di fine per la prelettura.</span><span class="sxs-lookup"><span data-stu-id="e87ea-126">The lengths of the end keys to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-127">rangeIndex</span><span class="sxs-lookup"><span data-stu-id="e87ea-127">rangeIndex</span></span>  
    <span data-ttu-id="e87ea-128">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e87ea-128">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e87ea-129">Indice del primo intervallo di chiavi nella matrice da leggere.</span><span class="sxs-lookup"><span data-stu-id="e87ea-129">The index of the first key range in the array to read.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-130">rangeCount</span><span class="sxs-lookup"><span data-stu-id="e87ea-130">rangeCount</span></span>  
    <span data-ttu-id="e87ea-131">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e87ea-131">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e87ea-132">Numero massimo di intervalli di chiavi da preleggere.</span><span class="sxs-lookup"><span data-stu-id="e87ea-132">The maximum number of key ranges to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-133">rangesPreread</span><span class="sxs-lookup"><span data-stu-id="e87ea-133">rangesPreread</span></span>  
    <span data-ttu-id="e87ea-134">Tipo: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="e87ea-134">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="e87ea-135">Restituisce il numero di chiavi effettivamente prelette.</span><span class="sxs-lookup"><span data-stu-id="e87ea-135">Returns the number of keys actually preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-136">columnsPreread</span><span class="sxs-lookup"><span data-stu-id="e87ea-136">columnsPreread</span></span>  
    <span data-ttu-id="e87ea-137">Tipo \[\]</span><span class="sxs-lookup"><span data-stu-id="e87ea-137">Type: \[\]</span></span>  
    
    <span data-ttu-id="e87ea-138">Elenco di ID di colonna per le colonne con valore esteso da preleggere.</span><span class="sxs-lookup"><span data-stu-id="e87ea-138">List of column ids for long value columns to preread.</span></span>

<!-- end list -->

  - <span data-ttu-id="e87ea-139">grbit</span><span class="sxs-lookup"><span data-stu-id="e87ea-139">grbit</span></span>  
    <span data-ttu-id="e87ea-140">Tipo: [Microsoft. ISAM. esent. Interop. Windows8. PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e87ea-140">Type: [Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit](./prereadindexrangesgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e87ea-141">Opzioni di prelettura.</span><span class="sxs-lookup"><span data-stu-id="e87ea-141">Preread options.</span></span> <span data-ttu-id="e87ea-142">Utilizzato per specificare la direzione della prelettura.</span><span class="sxs-lookup"><span data-stu-id="e87ea-142">Used to specify the direction of the preread.</span></span>

## <a name="see-also"></a><span data-ttu-id="e87ea-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e87ea-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e87ea-144">Riferimento</span><span class="sxs-lookup"><span data-stu-id="e87ea-144">Reference</span></span>

[<span data-ttu-id="e87ea-145">Classe Windows8Api</span><span class="sxs-lookup"><span data-stu-id="e87ea-145">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="e87ea-146">Membri di Windows8Api</span><span class="sxs-lookup"><span data-stu-id="e87ea-146">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="e87ea-147">Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="e87ea-147">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
