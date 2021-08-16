---
title: Funzione PlaySound
description: Funzione PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- audio multimediale, funzione PlaySound
- audio, funzione PlaySound
- audio waveform, funzione PlaySound
- Funzione PlaySound, informazioni
- Funzione sndPlaySound
- Funzione PlaySound, confrontata con la funzione sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1921ec4ef91f6266b48ee80d7f42be4540124c0b5c98dc18438ce0d16c398c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370851"
---
# <a name="the-playsound-function"></a>Funzione PlaySound

È possibile usare la [**funzione PlaySound**](/previous-versions//dd743680(v=vs.85)) per riprodurre audio waveform se il suono rientra nella memoria disponibile. La [**funzione sndPlaySound**](/previous-versions//dd798676(v=vs.85)) offre un subset delle funzionalità di PlaySound. Per ottimizzare la portabilità dell'applicazione basata su Win32, usare **PlaySound,** non **sndPlaySound.**

La **funzione PlaySound** consente di specificare un suono in uno dei tre modi seguenti:

-   Come avviso di sistema, usando l'alias archiviato nel file WIN.INI o nel Registro di sistema
-   Come nome file
-   Come identificatore di risorsa

La funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) consente di riprodurre un suono in un ciclo continuo, terminando solo quando si chiama di nuovo **PlaySound,** specificando **NULL** o l'identificatore del suono di un altro suono per il *parametro pszSound.*

È possibile usare **PlaySound** per riprodurre il suono in modo sincrono o asincrono e per controllare il comportamento della funzione in altri modi quando deve condividere le risorse di sistema.

Per altre informazioni sull'uso di PlaySound, vedere gli argomenti seguenti:

-   [Uso di PlaySound per riprodurre Waveform-Audio file](using-playsound-to-play-waveform-audio-files.md)
-   [Uso di PlaySound per riprodurre a ciclo continuo i suoni](using-playsound-to-loop-sounds.md)
-   [Uso di PlaySound per riprodurre suoni di sistema](using-playsound-to-play-system-sounds.md)

Per altri esempi di come usare **PlaySound** nelle applicazioni basate su Win32, vedere [Playing WAVE Resources (Riproduzione di risorse WAVE).](playing-wave-resources.md)

 

 