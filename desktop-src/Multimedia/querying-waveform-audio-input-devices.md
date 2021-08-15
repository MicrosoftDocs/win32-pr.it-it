---
title: Esecuzione di query Waveform-Audio dispositivi di input
description: Esecuzione di query Waveform-Audio dispositivi di input
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- audio waveform, query sui dispositivi di input
- interfaccia waveform-audio, esecuzione di query sui dispositivi di input
- registrazione dell'audio della forma d'onda, esecuzione di query sui dispositivi di input
- esecuzione di query su dispositivi di input waveform-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd22a2b65746202a831d475fcde38b31259619dbc645a5cbca3b91d03ff6e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371923"
---
# <a name="querying-waveform-audio-input-devices"></a>Esecuzione di query Waveform-Audio dispositivi di input

Prima di registrare l'audio della forma d'onda, è necessario chiamare la funzione [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) per determinare le funzionalità di input waveform-audio del sistema. Questa funzione riempie una [**struttura WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) con informazioni sulle funzionalità di un dispositivo specificato. Queste informazioni includono gli identificatori del produttore e del prodotto, il nome del prodotto per il dispositivo e il numero di versione del driver di dispositivo. Inoltre, la **struttura WAVEINCAPS** fornisce informazioni sui formati audio-forma d'onda standard supportati dal dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio waveform](recording-waveform-audio.md)
</dt> </dl>

 

 