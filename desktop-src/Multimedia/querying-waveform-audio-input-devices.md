---
title: Esecuzione di query sui dispositivi di input Waveform-Audio
description: Esecuzione di query sui dispositivi di input Waveform-Audio
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- audio Waveform, esecuzione di query sui dispositivi di input
- waveform-interfaccia audio, esecuzione di query sui dispositivi di input
- registrazione audio Waveform, esecuzione di query sui dispositivi di input
- esecuzione di query su dispositivi di input audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963021"
---
# <a name="querying-waveform-audio-input-devices"></a>Esecuzione di query sui dispositivi di input Waveform-Audio

Prima di registrare l'audio della forma d'onda, è necessario chiamare la funzione [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) per determinare le funzionalità di input dell'audio e della forma d'onda del sistema. Questa funzione riempie una struttura [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) con informazioni sulle funzionalità di un dispositivo specificato. Queste informazioni includono gli identificatori del produttore e del prodotto, il nome del prodotto per il dispositivo e il numero di versione del driver di dispositivo. Inoltre, la struttura **WAVEINCAPS** fornisce informazioni sui formati audio e di forma d'onda standard supportati dal dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio della forma d'onda](recording-waveform-audio.md)
</dt> </dl>

 

 