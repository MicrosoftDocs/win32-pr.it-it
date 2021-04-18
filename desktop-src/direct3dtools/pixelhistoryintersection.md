---
description: Rappresenta le informazioni su un particolare oggetto.
MS-HAID: vspixengine.PixelHistoryIntersection
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Struttura PixelHistoryIntersection
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: D67A116D-B1D0-4E88-A2FF-611CDF4003B2
api_name:
- PixelHistoryIntersection
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 735adc5396551a18b5e2e2dfba781b358289475e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304334"
---
# <a name="span-idvspixenginepixelhistoryintersectionspanpixelhistoryintersection-structure"></a><span id="vspixengine.pixelhistoryintersection"></span>Struttura PixelHistoryIntersection

Rappresenta le informazioni su un determinato oggetto

## <a name="syntax"></a>Sintassi


```C++
} PixelHistoryIntersection;
```

## <a name="members"></a>Members

**NumeroFrame**  
Frame dell'evento graphics associata con questa operazione.

**Eid**  
ID dell'evento di grafica associato a questa operazione.

**renderTargetPtr**  
Destinazione di rendering originariamente associata (all'interno dell'applicazione acquisita) con questa operazione.

**eventType**  
Tipo di evento associato a questa operazione (in particolare, se l'evento è una chiamata di tipo di progetto).

**punto**  
Coordinate del pixel nel framebuffer.

**bAssemblerStageGeneratesInstanceID**  
true se l'assembler di input genera gli ID istanza; in caso contrario, false.

**flags**  
Combinazione di valori PIXELHISTORYFLAGS. Per ulteriori informazioni, vedere l'enumerazione PIXELHISTORYFLAGS.

**fbInitialRed**  
Framebuffer: valore del componente colore rosso del framebuffer prima che venga eseguito il merge di qualsiasi pixel shader output; ovvero all'inizio del frame.

**fbInitialGreen**  
Framebuffer: valore del componente colore verde del framebuffer prima dell'Unione di qualsiasi pixel shader output; ovvero all'inizio del frame.

**fbInitialBlue**  
Framebuffer: valore del componente colore blu del framebuffer prima che venga eseguito il merge di qualsiasi pixel shader output; ovvero all'inizio del frame.

**fbInitialAlpha**  
Framebuffer: valore del componente a colori alfa del framebuffer prima dell'Unione di qualsiasi pixel shader output; ovvero all'inizio del frame.

**LabelFBInitialRed**  
Stringa COM contenente il nome dell'etichetta associata al componente colore rosso del framebuffer prima di qualsiasi ombreggiatura dei pixel; ovvero all'inizio del frame.

**LabelFBInitialGreen**  
Stringa COM contenente il nome dell'etichetta associata al componente colore verde del framebuffer prima di qualsiasi ombreggiatura dei pixel; ovvero all'inizio del frame.

**LabelFBInitialBlue**  
Stringa COM contenente il nome dell'etichetta associata al componente colore blu del framebuffer prima di qualsiasi ombreggiatura dei pixel; ovvero all'inizio del frame.

**LabelFBInitialAlpha**  
Stringa COM contenente il nome dell'etichetta associata al componente colore alfa del framebuffer prima di qualsiasi ombreggiatura dei pixel; ovvero all'inizio del frame.

**fbRed**  
Framebuffer: valore del componente colore rosso del framebuffer dopo l'Unione di tutti i pixel shader output; ovvero il colore del framebuffer finale.

**fbGreen**  
Framebuffer: valore del componente colore verde del framebuffer dopo l'Unione di tutti i pixel shader output; ovvero il colore del framebuffer finale.

**fbBlue**  
Framebuffer: valore del componente colore blu del framebuffer dopo l'Unione di tutti i pixel shader output; ovvero il colore del framebuffer finale.

**fbAlpha**  
Framebuffer: valore del componente a colori alfa del framebuffer dopo l'Unione di tutti i pixel shader output; ovvero il colore del framebuffer finale.

**LabelFBRed**  
Stringa COM contenente il nome dell'etichetta associata al componente colore rosso del framebuffer dopo l'ombreggiatura di tutti i pixel; ovvero il colore del framebuffer finale.

**LabelFBGreen**  
Stringa COM contenente il nome dell'etichetta associata al componente colore verde del framebuffer dopo l'ombreggiatura di tutti i pixel; ovvero il colore del framebuffer finale.

**LabelFBBlue**  
Stringa COM contenente il nome dell'etichetta associata al componente colore blu del framebuffer dopo l'ombreggiatura di tutti i pixel; ovvero il colore del framebuffer finale.

**LabelFBAlpha**  
Stringa COM contenente il nome dell'etichetta associata al componente colore alfa del framebuffer dopo l'ombreggiatura di tutti i pixel; ovvero il colore del framebuffer finale.

**pixelKillReason**  
Specifica il motivo per cui il contributo di colore del pixel è stato terminato.

**HResult**  
Se si è verificato un errore, contiene il valore HRESULT di DirectX che specifica l'errore.

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



