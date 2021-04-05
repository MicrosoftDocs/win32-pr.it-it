---
title: Buffer audio
description: Buffer audio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a67f120dc2d2ff956148e5dd4e3992a960641d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709178"
---
# <a name="audio-buffers"></a>Buffer audio

È possibile controllare la parte audio di un'operazione di acquisizione in tre modi:

-   Includere o escludere l'audio dall'operazione di acquisizione.
-   Richiedere un numero specifico di buffer audio.
-   Richiedere che i buffer audio siano di dimensioni specifiche.

È possibile recuperare le impostazioni per i buffer audio usando il messaggio di [**installazione della sequenza di WM \_ Cap \_ \_ \_ Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Il membro **fCaptureAudio** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) specifica se l'audio è incluso o escluso dall'operazione di acquisizione. Il numero di buffer audio richiesto corrente viene archiviato nel membro **wNumAudioRequested** e le dimensioni correnti del buffer audio sono archiviate nel membro **dwAudioBufferSize** . È possibile specificare se includere l'acquisizione audio, specificare le dimensioni e il numero di buffer audio aggiornando questi membri e inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio di [**\_ installazione della \_ \_ sequenza \_ di serie WM CAP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).

Per impostazione predefinita, l'audio è incluso nell'operazione di acquisizione e quattro buffer audio sono allocati. Il valore predefinito di **fCaptureAudio** è **true**. Le dimensioni predefinite del buffer (il valore di **dwAudioBufferSize**) possono contenere 0,5 secondi di dati audio o 10.000, a seconda del valore maggiore.

 

 




