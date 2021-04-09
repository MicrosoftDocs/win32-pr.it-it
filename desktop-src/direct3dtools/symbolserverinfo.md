---
description: Rappresenta le informazioni sul server dei simboli di debug.
MS-HAID: vspixengine.SymbolServerInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura SymbolServerInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D57D87E4-BA94-4C6F-9D5F-999C61F4DD6F
api_name:
- SymbolServerInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 65bf07a8ff915668c6c059b831bd049d9a25d9a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124155"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span data-ttu-id="0e9cc-103"><span id="vspixengine.symbolserverinfo"></span>Struttura SymbolServerInfo</span><span class="sxs-lookup"><span data-stu-id="0e9cc-103"><span id="vspixengine.symbolserverinfo"></span>SymbolServerInfo structure</span></span>

<span data-ttu-id="0e9cc-104">Rappresenta le informazioni sul server dei simboli di debug.</span><span class="sxs-lookup"><span data-stu-id="0e9cc-104">Represents information about the debug symbol server.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e9cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0e9cc-105">Syntax</span></span>


```C++
} SymbolServerInfo;
```

## <a name="members"></a><span data-ttu-id="0e9cc-106">Members</span><span class="sxs-lookup"><span data-stu-id="0e9cc-106">Members</span></span>

<span data-ttu-id="0e9cc-107">**symbolPath**</span><span class="sxs-lookup"><span data-stu-id="0e9cc-107">**symbolPath**</span></span>  
<span data-ttu-id="0e9cc-108">Stringa COM contenente il percorso del server di simboli.</span><span class="sxs-lookup"><span data-stu-id="0e9cc-108">A COM string containing the path of the symbol server.</span></span>

<span data-ttu-id="0e9cc-109">**symbolCacheDir**</span><span class="sxs-lookup"><span data-stu-id="0e9cc-109">**symbolCacheDir**</span></span>  
<span data-ttu-id="0e9cc-110">Stringa COM contenente la directory della cache del server di simboli.</span><span class="sxs-lookup"><span data-stu-id="0e9cc-110">A COM string containing the cache directory of the symbol server.</span></span>

<span data-ttu-id="0e9cc-111">**publicSymbolServerName**</span><span class="sxs-lookup"><span data-stu-id="0e9cc-111">**publicSymbolServerName**</span></span>  
<span data-ttu-id="0e9cc-112">Stringa COM contenente il nome pubblico del server di simboli.</span><span class="sxs-lookup"><span data-stu-id="0e9cc-112">A COM string containing the public name of the symbol server.</span></span>

<span data-ttu-id="0e9cc-113">**symbolExcludeList**</span><span class="sxs-lookup"><span data-stu-id="0e9cc-113">**symbolExcludeList**</span></span>  
<span data-ttu-id="0e9cc-114">Stringa COM che specifica l'elenco di simboli da escludere.</span><span class="sxs-lookup"><span data-stu-id="0e9cc-114">A COM string that specifies the list of symbols to exclude.</span></span>

<span data-ttu-id="0e9cc-115">**symbolIncludeList**</span><span class="sxs-lookup"><span data-stu-id="0e9cc-115">**symbolIncludeList**</span></span>  
<span data-ttu-id="0e9cc-116">Stringa COM che specifica l'elenco di simboli da includere.</span><span class="sxs-lookup"><span data-stu-id="0e9cc-116">A COM string that specifies the list of symbols to include.</span></span>

<span data-ttu-id="0e9cc-117">**useExcludeList**</span><span class="sxs-lookup"><span data-stu-id="0e9cc-117">**useExcludeList**</span></span>  
<span data-ttu-id="0e9cc-118">true se l'elenco di esclusioni viene ignorato; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="0e9cc-118">true if the exclude list is ignored; otherwise, false.</span></span>

<span data-ttu-id="0e9cc-119">**useMSSymbolServer**</span><span class="sxs-lookup"><span data-stu-id="0e9cc-119">**useMSSymbolServer**</span></span>  
<span data-ttu-id="0e9cc-120">true se si utilizza il server di simboli Microsoft; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="0e9cc-120">true if using Microsoft symbol server; otherwise, false.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e9cc-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0e9cc-121">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0e9cc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0e9cc-122">Header</span></span></p></td><td><span data-ttu-id="0e9cc-123">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="0e9cc-123">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



