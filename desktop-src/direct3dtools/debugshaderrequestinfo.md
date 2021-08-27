---
description: Rappresenta informazioni su una richiesta del debugger shader.
MS-HAID: vspixengine.DebugShaderRequestInfo
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura DebugShaderRequestInfo
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: DEFFAEE4-6C53-4C89-A533-A5BE73B80DEA
api_name:
- DebugShaderRequestInfo
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9691b13936ca8ec8e75aa02d9525a9d57143b19e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122628460"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span id="vspixengine.debugshaderrequestinfo"></span>Struttura DebugShaderRequestInfo

Rappresenta informazioni su una richiesta del debugger shader.

## <a name="syntax"></a>Sintassi


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a>Members

**Palco**  
Fase della pipeline di cui eseguire il debug.

**Eventid**  
ID dell'evento grafico di cui eseguire il debug.

**frameNumber**  
Frame di cui eseguire il debug.

**Vertice**  
Vertice di cui eseguire il debug.

**pixel**  
Pixel di cui eseguire il debug.

**groupCoordinates**  
Coordinate del gruppo di cui eseguire il debug.

**threadCoordinates**  
Coordinate del thread di cui eseguire il debug

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



