---
description: Rappresenta le informazioni sulla cronologia dei pixel.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PixelHistoryOperation
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304046"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>Struttura PixelHistoryOperation

Rappresenta le informazioni sulla cronologia dei pixel.

## <a name="syntax"></a>Sintassi


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>Members

**Eid**  
ID dell'evento di grafica associato a questa operazione.

**PCP**  
Chiamate compresse associate a questa operazione.

**renderTargetPtr**  
Destinazione di rendering originariamente associata (all'interno dell'applicazione acquisita) con questa operazione.

**iPrim**  
Indice della primitiva effettiva associata all'operazione.

**numPrims**  
Numero totale di primitive associate a questa operazione.

**numVertsPerPrim**  
Numero di vertici per primitive.

**iInstance**  
Quando si esegue il rendering di istanze, il numero di istanza dell'istanza effettiva associata a questa operazione.

**iInstanceCount**  
Quando si esegue il rendering di istanze, il numero totale di istanze associate a questa operazione.

**bAssemblerStageGeneratesInstanceID**  
true se l'assembler di input genera gli ID istanza; in caso contrario, false.

**flags**  
Combinazione di valori PIXELHISTORYFLAGS. Per ulteriori informazioni, vedere l'enumerazione PIXELHISTORYFLAGS.

**pVSFile**  
FILEPTR per il flusso di byte pixel shader. Questa operazione viene passata di nuovo per eseguire il debug.

**pGSFile**  
FILEPTR per il flusso di byte geometry shader. Questa operazione viene passata di nuovo per eseguire il debug.

**pPSFile**  
FILEPTR per il flusso di byte pixel shader. Questa operazione viene passata di nuovo per eseguire il debug.

**pHSFile**  
FILEPTR per il flusso di byte Hull shader. Questa operazione viene passata di nuovo per eseguire il debug.

**pDSFile**  
FILEPTR per il flusso di byte del dominio shader. Questa operazione viene passata di nuovo per eseguire il debug.

**pCSFile**  
FILEPTR per il flusso di byte compute shader. Questa operazione viene passata di nuovo per eseguire il debug.

**VertexShaderFile**  
Stringa COM contenente il percorso del file di origine del vertex shader.

**PixelShaderFile**  
Stringa COM contenente il percorso del file di origine del pixel shader.

**GeometryShaderFile**  
Stringa COM contenente il percorso del file di origine geometry shader.

**HullShaderFile**  
Stringa COM contenente il percorso del file di origine Hull shader.

**DomainShaderFile**  
Stringa COM contenente il percorso del file di origine del Domain shader.

**psRed**  
Output pixel shader: valore del componente colore rosso.

**psGreen**  
Output pixel shader: valore del componente colore verde.

**psBlue**  
Output pixel shader: valore del componente colore blu

**psAlpha**  
Output pixel shader: valore del componente colore alfa

**LabelPSRed**  
Stringa COM contenente il nome dell'etichetta associata al componente colore rosso dell'output del pixel shader.

**LabelPSGreen**  
Stringa COM contenente il nome dell'etichetta associata al componente colore verde dell'output del pixel shader.

**LabelPSBlue**  
Stringa COM contenente il nome dell'etichetta associata al componente colore blu dell'output del pixel shader.

**LabelPSAlpha**  
Stringa COM contenente il nome dell'etichetta associata al componente colore alfa dell'output del pixel shader.

**pixelKillReason**  
Output pixel shader: motivo per cui l'output del pixel è stato terminato.

**pixelOccluded**  
true se il pixel è nascosto; in caso contrario, false.

**fbRed**  
Framebuffer: valore del componente colore rosso del framebuffer prima che venga eseguito il merge pixel shader output.

**fbGreen**  
Framebuffer: valore del componente colore verde del framebuffer prima che venga eseguito il merge pixel shader output.

**fbBlue**  
Framebuffer: valore del componente colore blu del framebuffer prima che venga eseguito il merge pixel shader output.

**fbAlpha**  
Framebuffer: valore del componente a colori alfa del framebuffer prima del merge pixel shader output.

**LabelFBRed**  
Stringa COM contenente il nome dell'etichetta associata al componente colore rosso del framebuffer.

**LabelFBGreen**  
Stringa COM contenente il nome dell'etichetta associata al componente colore verde del framebuffer.

**LabelFBBlue**  
Stringa COM contenente il nome dell'etichetta associata al componente colore blu del framebuffer.

**LabelFBAlpha**  
Stringa COM contenente il nome dell'etichetta associata al componente colore alfa del framebuffer.

**topologia**  
Topologia dei vertici delle chiamate di richiamo (elenco di triangolo, striscia del triangolo e così via).

**vertici**  
Stringa COM contenente il buffer dei vertici a partire da questa primitiva. Il buffer dei vertici segue il formato di layout di input specificato nella fase della pipeline.

**vertexSize**  
Dimensioni in byte di un singolo vertice.

**InputLayout**  
Stringa COM contenente una sequenza di strutture InputLayoutStruct associate alla chiamata di progetto.

**HResult**  
HRESULT DirectX. In caso di problemi, questo può essere usato per visualizzare l'errore.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



