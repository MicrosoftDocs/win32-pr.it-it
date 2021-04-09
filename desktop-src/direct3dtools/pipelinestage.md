---
description: Rappresenta una fase della pipeline, inclusi i dettagli dello shader utilizzato.
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
ms.openlocfilehash: 5ddd0cbcf417da7967b135a10227ce6687cb2ea5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965627"
---
# <a name="span-idvspixenginepipelinestagespanpipelinestage-structure"></a><span id="vspixengine.pipelinestage"></span>Struttura PipeLineStage

Rappresenta una fase della pipeline, inclusi i dettagli dello shader utilizzato.

## <a name="syntax"></a>Sintassi


```C++
} PipeLineStage;
```

## <a name="members"></a>Members

**StageId**  
ID della fase della pipeline.

**Debuggable**  
true se la fase della pipeline supporta il debug; in caso contrario, false.

**StageName**  
Stringa COM contenente il nome della fase della pipeline.

**GuaranteedOutput**  
true se la fase della pipeline contiene sempre l'output della pipeline. in caso contrario, false.

**DebugEntryPoint**  
Stringa COM contenente il nome del punto di ingresso dello shader, se presente.

**ShaderFile**  
Stringa COM contenente il percorso del file di origine dello shader.

**ShaderByteStreamPtr**  
FILEPTR per il flusso di byte dello shader. Questa operazione viene passata di nuovo per eseguire il debug.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



