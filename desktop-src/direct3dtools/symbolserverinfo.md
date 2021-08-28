---
description: Rappresenta informazioni sul server di simboli di debug.
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
ms.openlocfilehash: 28f85445e6affc006c5c0898df1c85d71693a66d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632089"
---
# <a name="span-idvspixenginesymbolserverinfospansymbolserverinfo-structure"></a><span id="vspixengine.symbolserverinfo"></span>Struttura SymbolServerInfo

Rappresenta informazioni sul server di simboli di debug.

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
true se l'elenco di esclusione viene ignorato; in caso contrario, false.

**useMSSymbolServer**  
true se si usa il server di simboli Microsoft; in caso contrario, false.

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



