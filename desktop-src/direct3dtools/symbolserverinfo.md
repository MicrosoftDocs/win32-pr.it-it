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
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>Struttura SymbolServerInfo

Rappresenta le informazioni sul server dei simboli di debug.

## <a name="syntax"></a>Sintassi


```C++
} SymbolServerInfo;
```

## <a name="members"></a>Members

**symbolPath**  
Stringa COM contenente il percorso del server di simboli.

**symbolCacheDir**  
Stringa COM contenente la directory della cache del server di simboli.

**publicSymbolServerName**  
Stringa COM contenente il nome pubblico del server di simboli.

**symbolExcludeList**  
Stringa COM che specifica l'elenco di simboli da escludere.

**symbolIncludeList**  
Stringa COM che specifica l'elenco di simboli da includere.

**useExcludeList**  
true se l'elenco di esclusioni viene ignorato; in caso contrario, false.

**useMSSymbolServer**  
true se si utilizza il server di simboli Microsoft; in caso contrario, false.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



