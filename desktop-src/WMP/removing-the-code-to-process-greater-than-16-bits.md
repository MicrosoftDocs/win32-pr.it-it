---
title: Rimozione del codice per elaborare più di 16 bit
description: Rimozione del codice per elaborare più di 16 bit
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Plug-in di Windows Media Player, metodo DoProcessOutput di esempio Echo
- plug-in, esempio Echo metodo DoProcessOutput
- plug-in di elaborazione dei segnali digitali, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
- Esempio di plug-in Echo DSP, elaborazione superiore a 16 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec33332ee332d0ca7b615844ba8ad5cd7b00eb2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856182"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a>Rimozione del codice per elaborare più di 16 bit

Poiché questo esempio elabora solo l'audio a 8 bit o a 16 bit, è necessario modificare il codice in **CEcho:: ValidateMediaType** per restituire il \_ tipo DMO E \_ \_ non \_ accettato per i tipi di supporti maggiori di 16 bit. A tale scopo, è necessario modificare il codice nel blocco switch che testa i formati di tipo WAVE \_ Format \_ estensibile. Sostituire il codice della procedura guidata con il codice di esempio seguente:


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



A questo punto, eliminare o impostare come commento le sezioni di codice in **DoProcessOutput** che gestiscono audio di risoluzione del bit elevato. Queste sono le sezioni che iniziano con il caso 24 e il caso 32.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di CEcho::D oProcessOutput**](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




