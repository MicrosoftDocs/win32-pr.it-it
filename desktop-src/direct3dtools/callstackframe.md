---
description: Rappresenta informazioni su un frame sullock chiamate.
MS-HAID: vspixengine.CallStackFrame
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura CallStackFrame
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 50941BA0-968D-4341-8BF5-854FBDE8BD0C
api_name:
- CallStackFrame
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c6cb4b0e32213165149d7df8c7bf334049e37399
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631339"
---
# <a name="span-idvspixenginecallstackframespancallstackframe-structure"></a><span id="vspixengine.callstackframe"></span>Struttura CallStackFrame

Rappresenta informazioni su un frame sullock chiamate.

## <a name="syntax"></a>Sintassi


```C++
} CallStackFrame;
```

## <a name="members"></a>Members

**Functionname**  
Stringa COM contenente il nome della funzione associata.

**sourceFile**  
Stringa COM contenente il percorso del file di origine associato.

**Modulename**  
Stringa COM contenente il nome del modulo di codice associato.

**Linenumber**  
Numero di riga associato.

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



