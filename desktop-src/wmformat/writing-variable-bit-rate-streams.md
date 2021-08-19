---
title: Scrittura di velocità in bit variabile Flussi
description: Scrittura di velocità in bit variabile Flussi
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Advanced Systems Format (ASF), scrittura di flussi VBR
- ASF (Advanced Systems Format), scrittura di flussi VBR
- velocità in bit variabile (VBR), scrittura di flussi
- VBR (velocità in bit variabile),scrittura di flussi
- flussi, scrittura vbr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 694774613ada8b4be05eab55be3213898d423d3b6ac4438204d149a0bd606c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930259"
---
# <a name="writing-variable-bit-rate-streams"></a>Scrittura di velocità in bit variabile Flussi

I flussi vbr (Variable Bit Rate) vengono scritti nello stesso modo dei flussi CBR (Constant Bit Rate). L'unica differenza consiste nell'elaborazione eseguita internamente dal writer e dai codec. Tuttavia, vbr basato sulla velocità in bit (sia vincolato che non vincolato) richiede un passaggio di pre-elaborazione nel writer.

È necessario controllare il valore restituito per la prima chiamata a [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) per ogni flusso. Se il codice di errore restituito è NS \_ E \_ INVALID NUM \_ \_ PASSES, il flusso richiede un passaggio di pre-elaborazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso Two-Pass codifica**](using-two-pass-encoding.md)
</dt> <dt>

[**Scrittura di file ASF**](writing-asf-files.md)
</dt> </dl>

 

 




