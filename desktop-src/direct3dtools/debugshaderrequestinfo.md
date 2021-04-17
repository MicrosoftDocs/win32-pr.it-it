---
description: Rappresenta le informazioni su una richiesta del debugger shader.
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
ms.openlocfilehash: a59bfb84bb7d4e8644c0cfadc4475be7d7da4a54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521586"
---
# <a name="span-idvspixenginedebugshaderrequestinfospandebugshaderrequestinfo-structure"></a><span id="vspixengine.debugshaderrequestinfo"></span>Struttura DebugShaderRequestInfo

Rappresenta le informazioni su una richiesta del debugger shader.

## <a name="syntax"></a>Sintassi


```C++
} DebugShaderRequestInfo;
```

## <a name="members"></a>Members

**fase**  
Fase della pipeline di cui eseguire il debug.

**eventID**  
ID dell'evento di grafica di cui eseguire il debug.

**NumeroFrame**  
Frame di cui eseguire il debug.

**vertice**  
Vertice di cui eseguire il debug.

**pixel**  
Pixel di cui eseguire il debug.

**groupCoordinates**  
Coordinate del gruppo di cui eseguire il debug.

**threadCoordinates**  
Coordinate del thread di cui eseguire il debug

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



