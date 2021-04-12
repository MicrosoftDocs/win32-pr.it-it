---
title: Funzione PlaySound
description: Funzione PlaySound
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- audio multimediale, funzione PlaySound
- audio, funzione PlaySound
- audio Waveform, funzione PlaySound
- PlaySound (funzione), informazioni
- sndPlaySound (funzione)
- Funzione PlaySound, confrontata con la funzione sndPlaySound
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104223537"
---
# <a name="the-playsound-function"></a>Funzione PlaySound

È possibile usare la funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) per riprodurre l'audio della forma d'onda se il suono si adatta alla memoria disponibile. La funzione [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) offre un subset delle funzionalità di PlaySound. Per ottimizzare la portabilità dell'applicazione basata su Win32, usare **PlaySound**, non **sndPlaySound**.

La funzione **PlaySound** consente di specificare un suono in uno dei tre modi seguenti:

-   Come avviso di sistema, usando l'alias archiviato nel file WIN.INI o nel registro di sistema
-   Come nome file
-   Come identificatore di risorsa

La funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) consente di riprodurre un suono in un ciclo continuo, terminando solo quando si chiama di nuovo **PlaySound** , specificando **null** o l'identificatore audio di un altro suono per il parametro *pszSound* .

È possibile usare **PlaySound** per riprodurre il suono in modo sincrono o asincrono e per controllare il comportamento della funzione in altri modi quando deve condividere le risorse di sistema.

Per ulteriori informazioni sull'utilizzo di PlaySound, vedere gli argomenti seguenti:

-   [Uso di PlaySound per riprodurre file di Waveform-Audio](using-playsound-to-play-waveform-audio-files.md)
-   [Uso di PlaySound per il ciclo di suoni](using-playsound-to-loop-sounds.md)
-   [Uso di PlaySound per riprodurre suoni di sistema](using-playsound-to-play-system-sounds.md)

Per altri esempi su come usare **PlaySound** nelle applicazioni basate su Win32, vedere la pagina relativa alla [riproduzione di risorse Wave](playing-wave-resources.md).

 

 