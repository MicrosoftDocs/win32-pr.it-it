---
description: Rappresenta una fase della pipeline, inclusi i dettagli dello shader usato.
MS-HAID: vspixengine.PipeLineStage
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PipeLineStage
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 616103CB-777E-4AA8-8B70-E19B1A2D667C
api_name:
- PipeLineStage
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10f1d1780404303109a72fe1a12023bc35b2c0ca
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625167"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>Struttura PipeLineStage

Rappresenta una fase della pipeline, inclusi i dettagli dello shader usato.

## <a name="syntax"></a>Sintassi


```C++
} PipeLineStage;
```

## <a name="members"></a>Members

**Id fase**  
ID della fase della pipeline.

**Debuggable**  
true se la fase della pipeline supporta il debug; in caso contrario, false.

**StageName**  
Stringa COM contenente il nome della fase della pipeline.

**Output garantito**  
true se la fase della pipeline include sempre l'output della pipeline; in caso contrario, false.

**DebugEntryPoint**  
Stringa COM contenente il nome del punto di ingresso dello shader, se presente.

**ShaderFile**  
Stringa COM contenente il percorso del file di origine dello shader.

**ShaderByteStreamPtr**  
Oggetto FILEPTR per il flusso di byte dello shader. Viene passato nuovamente per eseguire il debug.

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



