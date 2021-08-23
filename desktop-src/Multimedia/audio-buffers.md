---
title: Buffer audio
description: Buffer audio
ms.assetid: e18e9ff4-e8e9-4013-a800-1a30335026ff
keywords:
- WM_CAP_GET_SEQUENCE_SETUP messaggio
- Macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP messaggio
- Macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7993e3dc89abda520c0f1c5bda90f3eb209aca31e36071a304af01fb420d821e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692101"
---
# <a name="audio-buffers"></a>Buffer audio

È possibile controllare la parte audio di un'operazione di acquisizione in tre modi:

-   Includere o escludere l'audio dall'operazione di acquisizione.
-   Richiedere un numero specifico di buffer audio.
-   Richiedere che i buffer audio siano di dimensioni specifiche.

È possibile recuperare le impostazioni per i buffer audio usando il messaggio [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Il **membro fCaptureAudio** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) specifica se l'audio è incluso o escluso dall'operazione di acquisizione. Il numero corrente di buffer audio richiesti viene archiviato nel membro **wNumAudioRequested** e le dimensioni correnti del buffer audio vengono archiviate nel membro **dwAudioBufferSize.** È possibile specificare se includere l'acquisizione audio, specificare le dimensioni e il numero di buffer audio aggiornando questi membri e inviare la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup)

Per impostazione predefinita, l'audio è incluso nell'operazione di acquisizione e vengono allocati quattro buffer audio. Il valore predefinito di **fCaptureAudio** è **TRUE.** Le dimensioni predefinite del buffer (il valore **di dwAudioBufferSize**) possono contenere 0,5 secondi di dati audio o 10.000, a seconda del valore maggiore.

 

 




