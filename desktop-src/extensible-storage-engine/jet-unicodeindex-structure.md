---
description: 'Altre informazioni su: struttura JET_UNICODEINDEX'
title: Struttura JET_UNICODEINDEX
TOCTitle: JET_UNICODEINDEX Structure
ms:assetid: d0b8ef74-850e-4e21-9f71-b56ec472aa0f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294097(v=EXCHG.10)
ms:contentKeyID: 32765712
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4a2332551fb1f624b75e32596b2941d97ffa47d
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "104402038"
---
# <a name="jet_unicodeindex-structure"></a><span data-ttu-id="51e6f-103">Struttura JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="51e6f-103">JET_UNICODEINDEX Structure</span></span>


<span data-ttu-id="51e6f-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="51e6f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_unicodeindex-structure"></a><span data-ttu-id="51e6f-105">Struttura JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="51e6f-105">JET_UNICODEINDEX Structure</span></span>

<span data-ttu-id="51e6f-106">La struttura **JET_UNICODEINDEX** Personalizza il modo in cui i dati Unicode vengono normalizzati quando viene creato un indice su una colonna Unicode.</span><span class="sxs-lookup"><span data-stu-id="51e6f-106">The **JET_UNICODEINDEX** structure customizes how Unicode data gets normalized when an index is created over a Unicode column.</span></span>

```cpp
typedef struct tagJET_UNICODEINDEX {
  unsigned long lcid;
  unsigned long dwMapFlags;
} JET_UNICODEINDEX;
```

### <a name="members"></a><span data-ttu-id="51e6f-107">Membri</span><span class="sxs-lookup"><span data-stu-id="51e6f-107">Members</span></span>

<span data-ttu-id="51e6f-108">**lcid**</span><span class="sxs-lookup"><span data-stu-id="51e6f-108">**lcid**</span></span>

<span data-ttu-id="51e6f-109">ID delle impostazioni locali da utilizzare per la normalizzazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="51e6f-109">The Locale ID to use when normalizing the data.</span></span> <span data-ttu-id="51e6f-110">Le impostazioni locali possono essere usate purché nel computer sia installato il Language Pack appropriato.</span><span class="sxs-lookup"><span data-stu-id="51e6f-110">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span> <span data-ttu-id="51e6f-111">L'unica eccezione è che le impostazioni locali indipendenti dalla lingua (LCID di zero) non sono valide.</span><span class="sxs-lookup"><span data-stu-id="51e6f-111">The one exception is that the Language Neutral locale (LCID of zero) is illegal.</span></span>

<span data-ttu-id="51e6f-112">**dwMapFlags**</span><span class="sxs-lookup"><span data-stu-id="51e6f-112">**dwMapFlags**</span></span>

<span data-ttu-id="51e6f-113">Questi flag vengono passati a [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) quando i dati Unicode vengono normalizzati in una chiave, che consente ai flag definiti dall'utente di eseguire l'override del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="51e6f-113">These flags get passed to [LCMapString](/windows/win32/api/winnls/nf-winnls-lcmapstringa) when Unicode data gets normalized to a key, which enables user-defined flags to override the default.</span></span>

<span data-ttu-id="51e6f-114">**Windows 2000**: gli unici due valori validi per **dwFlags** sono:</span><span class="sxs-lookup"><span data-stu-id="51e6f-114">**Windows 2000**:  The only two legal values for **dwFlags** are:</span></span>

  - <span data-ttu-id="51e6f-115">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE)</span><span class="sxs-lookup"><span data-stu-id="51e6f-115">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH | NORM_IGNORENONSPACE )</span></span>

<!-- end list -->

  - <span data-ttu-id="51e6f-116">(LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH)</span><span class="sxs-lookup"><span data-stu-id="51e6f-116">( LCMAP_SORTKEY | NORM_IGNORECASE | NORM_IGNOREKANATYPE | NORM_IGNOREWIDTH )</span></span>

<span data-ttu-id="51e6f-117">**dwMapFlags** presenta le restrizioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="51e6f-117">**dwMapFlags** has the following restrictions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51e6f-118">Valore</span><span class="sxs-lookup"><span data-stu-id="51e6f-118">Value</span></span></p></th>
<th><p><span data-ttu-id="51e6f-119">Significato</span><span class="sxs-lookup"><span data-stu-id="51e6f-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51e6f-120">LCMAP_SORTKEY</span><span class="sxs-lookup"><span data-stu-id="51e6f-120">LCMAP_SORTKEY</span></span></p></td>
<td><p><span data-ttu-id="51e6f-121">Mandatory.</span><span class="sxs-lookup"><span data-stu-id="51e6f-121">Mandatory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51e6f-122">LCMAP_BYTEREV</span><span class="sxs-lookup"><span data-stu-id="51e6f-122">LCMAP_BYTEREV</span></span></p></td>
<td><p><span data-ttu-id="51e6f-123">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="51e6f-123">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51e6f-124">NORM_IGNORECASE</span><span class="sxs-lookup"><span data-stu-id="51e6f-124">NORM_IGNORECASE</span></span></p></td>
<td><p><span data-ttu-id="51e6f-125">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="51e6f-125">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51e6f-126">NORM_IGNORENONSPACE</span><span class="sxs-lookup"><span data-stu-id="51e6f-126">NORM_IGNORENONSPACE</span></span></p></td>
<td><p><span data-ttu-id="51e6f-127">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="51e6f-127">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51e6f-128">NORM_IGNORESYMBOLS</span><span class="sxs-lookup"><span data-stu-id="51e6f-128">NORM_IGNORESYMBOLS</span></span></p></td>
<td><p><span data-ttu-id="51e6f-129">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="51e6f-129">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51e6f-130">NORM_IGNOREKANATYPE</span><span class="sxs-lookup"><span data-stu-id="51e6f-130">NORM_IGNOREKANATYPE</span></span></p></td>
<td><p><span data-ttu-id="51e6f-131">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="51e6f-131">Optional.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51e6f-132">NORM_IGNOREWIDTH</span><span class="sxs-lookup"><span data-stu-id="51e6f-132">NORM_IGNOREWIDTH</span></span></p></td>
<td><p><span data-ttu-id="51e6f-133">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="51e6f-133">Optional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51e6f-134">SORT_STRINGSORT</span><span class="sxs-lookup"><span data-stu-id="51e6f-134">SORT_STRINGSORT</span></span></p></td>
<td><p><span data-ttu-id="51e6f-135">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="51e6f-135">Optional.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="51e6f-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51e6f-136">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51e6f-137"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="51e6f-137"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="51e6f-138">Richiede Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="51e6f-138">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51e6f-139"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="51e6f-139"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="51e6f-140">Richiede Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="51e6f-140">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51e6f-141"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="51e6f-141"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="51e6f-142">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="51e6f-142">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="51e6f-143">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="51e6f-143">See Also</span></span>

[<span data-ttu-id="51e6f-144">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="51e6f-144">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="51e6f-145">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="51e6f-145">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="51e6f-146">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="51e6f-146">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)
