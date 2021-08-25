---
title: Uso di PlaySound per riprodurre suoni di sistema
description: Uso di PlaySound per riprodurre suoni di sistema
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- audio waveform, funzione PlaySound
- audio waveform, riproduzione di suoni di sistema
- audio waveform, eventi audio
- Funzione PlaySound, riproduzione di suoni di sistema
- Funzione PlaySound, eventi audio
- riproduzione di suoni di sistema audio-forma d'onda
- eventi audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9978e9e33c049db82a033b2379ac9f52b5e2959fd9d8425deac180ba7a81e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804571"
---
# <a name="using-playsound-to-play-system-sounds"></a>Uso di PlaySound per riprodurre suoni di sistema

La [**funzione PlaySound**](/previous-versions//dd743680(v=vs.85)) riprodurrà anche i suoni a cui fa riferimento un nome di chiave nel Registro di sistema. Gli utenti possono assegnare i propri suoni agli avvisi di sistema o alle azioni dell'utente, ad esempio il clic di un pulsante del mouse. I suoni associati agli avvisi di sistema e agli avvisi sono detti *eventi audio.*

Per riprodurre un evento audio, chiamare **PlaySound** con il parametro *pszSound* che punta a una stringa contenente il nome della voce del Registro di sistema che identifica il suono. Ad esempio, per riprodurre il suono associato alla voce "MouseClick" e attendere il completamento del suono prima della restituzione, usare l'istruzione seguente:


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



Se la voce del Registro di sistema specificata o il file audio waveform identificato non esiste o se il file non rientra nella memoria disponibile, **PlaySound** riproduce il suono di sistema predefinito.

Gli eventi audio predefiniti dal sistema possono variare in base alla piattaforma. L'elenco seguente fornisce gli eventi audio definiti per tutte le implementazioni dell'API Win32:

-   SystemAsterisk
-   SystemExclamation
-   SystemExit
-   SystemHand
-   SystemQuestion
-   Avvio del sistema

Se un'applicazione registra i propri eventi audio, l'utente può configurare l'evento audio usando l'interfaccia Pannello di controllo standard. L'applicazione deve registrare l'evento audio usando le funzioni standard del Registro di sistema. Per altre informazioni, vedere [Registro di sistema.](../sysinfo/registry.md) Le voci appartengono alla stessa posizione nella gerarchia del Registro di sistema del resto degli eventi audio. Questa posizione varia in base all'implementazione Win32. Il valore dei dati appropriato varia anche in base all'implementazione di .

La [**funzione sndPlaySound**](/previous-versions//dd798676(v=vs.85)) cerca sempre nel Registro di sistema un nome di chiave corrispondente a *lpszSound* prima di tentare di caricare un file con questo nome. La [**funzione PlaySound**](/previous-versions//dd743680(v=vs.85)) accetta flag che specificano la posizione del suono.

 

 