---
description: Rappresenta informazioni sulla cronologia pixel.
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
ms.openlocfilehash: 15cae4986b7dc109c08011d2cc23e1b6133de9e5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625187"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>Struttura PixelHistoryOperation

Rappresenta informazioni sulla cronologia pixel.

## <a name="syntax"></a>Sintassi


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>Members

**Eid**  
ID dell'evento grafico associato a questa operazione.

**PCP**  
Chiamate di tipo pack associate a questa operazione.

**renderTargetPtr**  
Destinazione di rendering originariamente associata (all'interno dell'applicazione acquisita) a questa operazione.

**iPrim**  
Indice della primitiva effettiva associata all'operazione.

**numPrims**  
Numero totale di primitive associate a questa operazione.

**numVertsPerPrim**  
Numero di vertici per primitiva.

**iInstance**  
Quando si esegue il rendering delle istanze di , il numero di istanza dell'istanza effettiva associata a questa operazione.

**iInstanceCount**  
Quando si esegue il rendering delle istanze, il numero totale di istanze associate a questa operazione.

**bAssemblerStageGeneratesInstanceID**  
true se l'assembler di input genera ID istanza; in caso contrario, false.

**flags**  
Combinazione di valori PIXELHISTORYFLAGS. Per altre informazioni, vedere l'enumerazione PIXELHISTORYFLAGS.

**pVSFile**  
Oggetto FILEPTR per il flusso pixel shader byte specificato. Viene passato nuovamente per eseguire il debug.

**pGSFile**  
OGGETTO FILEPTR per il flusso di byte dello shader geometrico. Viene passato nuovamente per eseguire il debug.

**pPSFile**  
Oggetto FILEPTR per il flusso pixel shader byte specificato. Viene passato nuovamente per eseguire il debug.

**pHSFile**  
OGGETTO FILEPTR per il flusso di byte dello shader di tipo hull. Viene passato nuovamente per eseguire il debug.

**pDSFile**  
Oggetto FILEPTR per il flusso di byte dello shader del dominio. Viene passato nuovamente per eseguire il debug.

**pCSFile**  
Oggetto FILEPTR per il flusso di byte compute shader. Viene passato nuovamente per eseguire il debug.

**VertexShaderFile**  
Stringa COM contenente il percorso del file di origine del vertex shader.

**PixelShaderFile**  
Stringa COM contenente il percorso del file di pixel shader di origine.

**GeometryShaderFile**  
Stringa COM contenente il percorso del file di origine geometry shader.

**HullShaderFile**  
Stringa COM contenente il percorso del file di origine dello shader di tipo hull.

**DomainShaderFile**  
Stringa COM contenente il percorso del file di origine dello shader del dominio.

**psRed**  
Output del pixel shader: valore del componente di colore rosso.

**psGreen**  
Output del pixel shader: valore del componente colore verde.

**psBlue**  
Output del pixel shader: valore del componente colore blu

**psAlpha**  
Output del pixel shader: valore del componente colore alfa

**LabelPSRed**  
Stringa COM contenente il nome dell'etichetta associata al componente di colore rosso del pixel shader output.

**LabelPSGreen**  
Stringa COM contenente il nome dell'etichetta associata al componente di colore verde del pixel shader output.

**LabelPSBlue**  
Stringa COM contenente il nome dell'etichetta associata al componente di colore blu dell pixel shader output.

**LabelPSAlpha**  
Stringa COM contenente il nome dell'etichetta associata al componente del colore alfa dell pixel shader output.

**pixelKillReason**  
Output del pixel shader: motivo per cui l'output del pixel è stato finale.

**pixelOccluded**  
true se il pixel è occluded; in caso contrario, false.

**fbRed**  
Framebuffer: valore del componente di colore rosso di framebuffer prima pixel shader'output viene unito.

**fbGreen**  
Framebuffer: valore del componente di colore verde di framebuffer prima pixel shader'output viene unito.

**fbBlue**  
Framebuffer: valore del componente di colore blu di framebuffer prima pixel shader'output viene unito.

**fbAlpha**  
Framebuffer: valore del componente di colore alfa di framebuffer prima pixel shader'output viene unito.

**LabelFBRed**  
Stringa COM contenente il nome dell'etichetta associata al componente di colore rosso di framebuffer.

**LabelFBGreen**  
Stringa COM contenente il nome dell'etichetta associata al componente di colore verde di framebuffer.

**LabelFBBlue**  
Stringa COM contenente il nome dell'etichetta associata al componente di colore blu di framebuffer.

**LabelFBAlpha**  
Stringa COM contenente il nome dell'etichetta associata al componente di colore alfa di framebuffer.

**Topologia**  
Topologia dei vertici delle chiamate di disegno (elenco di triangoli, striscia di triangoli e così via).

**Vertici**  
Stringa COM contenente il buffer dei vertici a partire da questa primitiva. Il buffer dei vertici segue il formato di layout di input specificato nella fase della pipeline.

**vertexSize**  
Dimensione di un singolo vertice in byte.

**InputLayout**  
Stringa COM contenente una sequenza di strutture InputLayoutStruct associate alla chiamata di disegno.

**Hresult**  
Hresult DirectX. In caso di problemi, è possibile usare questa opzione per visualizzare l'errore.

## <a name="requirements"></a>Requisiti

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



