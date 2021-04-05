---
description: 'Altre informazioni su: struttura JET_ERRINFOBASIC_W'
title: Struttura JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/16/2021
ms.locfileid: "103969534"
---
# <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="c14fa-103">Struttura JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="c14fa-103">JET_ERRINFOBASIC_W Structure</span></span>


<span data-ttu-id="c14fa-104">_**Si applica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c14fa-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errinfobasic_w-structure"></a><span data-ttu-id="c14fa-105">Struttura JET_ERRINFOBASIC_W</span><span class="sxs-lookup"><span data-stu-id="c14fa-105">JET_ERRINFOBASIC_W Structure</span></span>

<span data-ttu-id="c14fa-106">La struttura **JET_ERRINFOBASIC_W** definisce i dati restituiti dal metodo [JetGetErrorInfo ()](./jetgeterrorinfow-function.md) quando il JET_ErrorInfoSpecificErr InfoLevel viene passato.</span><span class="sxs-lookup"><span data-stu-id="c14fa-106">The **JET_ERRINFOBASIC_W** structure defines the data that is returned from the [JetGetErrorInfo()](./jetgeterrorinfow-function.md) method when the JET_ErrorInfoSpecificErr InfoLevel is passed in.</span></span>

<span data-ttu-id="c14fa-107">Nota: questa documentazione si basa su una versione preliminare del motore di archiviazione estendibile.</span><span class="sxs-lookup"><span data-stu-id="c14fa-107">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="c14fa-108">Queste informazioni sono soggette a modifiche.</span><span class="sxs-lookup"><span data-stu-id="c14fa-108">This information is subject to change.</span></span>

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a><span data-ttu-id="c14fa-109">Membri</span><span class="sxs-lookup"><span data-stu-id="c14fa-109">Members</span></span>

<span data-ttu-id="c14fa-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="c14fa-110">**cbStruct**</span></span>

<span data-ttu-id="c14fa-111">Dimensioni, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="c14fa-111">The size of the structure, in bytes.</span></span> <span data-ttu-id="c14fa-112">Deve essere impostato su sizeof (JET_ERRINFOBASIC).</span><span class="sxs-lookup"><span data-stu-id="c14fa-112">It must be set to sizeof( JET_ERRINFOBASIC ).</span></span>

<span data-ttu-id="c14fa-113">**errValue**</span><span class="sxs-lookup"><span data-stu-id="c14fa-113">**errValue**</span></span>

<span data-ttu-id="c14fa-114">Valore di errore valutato, come passato per l'argomento *pvResult* a [JetGetErrorInfo ()](./jetgeterrorinfow-function.md).</span><span class="sxs-lookup"><span data-stu-id="c14fa-114">The error value that was evaluated, as passed in for the *pvResult* argument to [JetGetErrorInfo()](./jetgeterrorinfow-function.md).</span></span>

<span data-ttu-id="c14fa-115">**errcatMostSpecific**</span><span class="sxs-lookup"><span data-stu-id="c14fa-115">**errcatMostSpecific**</span></span>

<span data-ttu-id="c14fa-116">Costante [JET_ERRCAT](./jet-errcat.md) di livello più basso associata all'errore. ovvero la categoria a livello foglia nella gerarchia delle categorie documentata in [JET_ERRCAT](./jet-errcat.md).</span><span class="sxs-lookup"><span data-stu-id="c14fa-116">The lowest-level [JET_ERRCAT](./jet-errcat.md) constant that is associated with the error; that is, the leaf-level category in the category hierarchy documented in [JET_ERRCAT](./jet-errcat.md).</span></span>

<span data-ttu-id="c14fa-117">**rgCategoricalHierarchy \[ 8\]**</span><span class="sxs-lookup"><span data-stu-id="c14fa-117">**rgCategoricalHierarchy\[8\]**</span></span>

<span data-ttu-id="c14fa-118">Gerarchia delle categorie di errore associata all'errore.</span><span class="sxs-lookup"><span data-stu-id="c14fa-118">The hierarchy of error categories that is associated with the error.</span></span> <span data-ttu-id="c14fa-119">La posizione 0 è il livello più alto nella gerarchia di [JET_ERRCAT](./jet-errcat.md)e le altre sono sottocategorie fino a quando non viene impostata la categoria più specifica, dopo le quali vengono JET_errcatUnknown tutte le categorie.</span><span class="sxs-lookup"><span data-stu-id="c14fa-119">Position 0 is the highest level in the hierarchy of [JET_ERRCAT](./jet-errcat.md), and the rest are subcategories until the most specific category is set, after which all categories are JET_errcatUnknown.</span></span>

<span data-ttu-id="c14fa-120">**lSourceLine**</span><span class="sxs-lookup"><span data-stu-id="c14fa-120">**lSourceLine**</span></span>

<span data-ttu-id="c14fa-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c14fa-121">Reserved.</span></span>

<span data-ttu-id="c14fa-122">**rgszSourceFile \[ 64\]**</span><span class="sxs-lookup"><span data-stu-id="c14fa-122">**rgszSourceFile\[64\]**</span></span>

<span data-ttu-id="c14fa-123">Riservato.</span><span class="sxs-lookup"><span data-stu-id="c14fa-123">Reserved.</span></span>

### <a name="requirements"></a><span data-ttu-id="c14fa-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c14fa-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c14fa-125"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="c14fa-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c14fa-126">Richiede Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c14fa-126">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c14fa-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c14fa-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c14fa-128">Richiede Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="c14fa-128">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c14fa-129"><strong>Intestazione</strong></span><span class="sxs-lookup"><span data-stu-id="c14fa-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c14fa-130">Dichiarata in esent. h.</span><span class="sxs-lookup"><span data-stu-id="c14fa-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>
