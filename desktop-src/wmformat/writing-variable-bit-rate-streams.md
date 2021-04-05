---
title: Scrittura di flussi di velocità in bit variabili
description: Scrittura di flussi di velocità in bit variabili
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Formato di sistemi avanzati (ASF), scrittura di flussi VBR
- ASF (Advanced Systems Format), scrittura di flussi VBR
- velocità in bit variabile (VBR), scrittura di flussi
- VBR (velocità in bit variabile), scrittura di flussi
- flussi, scrittura di VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723391"
---
# <a name="writing-variable-bit-rate-streams"></a>Scrittura di flussi di velocità in bit variabili

I flussi di velocità in bit variabile (VBR) vengono scritti allo stesso modo dei flussi di velocità in bit costante (CBR). L'unica differenza è rappresentata dall'elaborazione eseguita internamente dal writer e dai codec. Tuttavia, la velocità in bit basata su VBR (sia vincolata che non vincolata) richiede un passaggio di pre-elaborazione nel writer.

È necessario controllare il valore restituito per la prima chiamata a [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) per ogni flusso. Se il codice di errore restituito è NS E il numero di \_ \_ passaggi non è valido \_ \_ , il flusso richiede un passaggio di pre-elaborazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso della codifica Two-Pass**](using-two-pass-encoding.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




