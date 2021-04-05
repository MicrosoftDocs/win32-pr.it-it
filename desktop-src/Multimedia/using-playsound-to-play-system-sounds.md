---
title: Uso di PlaySound per riprodurre suoni di sistema
description: Uso di PlaySound per riprodurre suoni di sistema
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- audio Waveform, funzione PlaySound
- audio Waveform, riproduzione di suoni di sistema
- audio Waveform, eventi audio
- Funzione PlaySound, riproduzione di suoni di sistema
- Funzione PlaySound, eventi audio
- riproduzione di suoni di sistema Waveform
- eventi audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872513"
---
# <a name="using-playsound-to-play-system-sounds"></a>Uso di PlaySound per riprodurre suoni di sistema

La funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) riprodurrà anche i suoni a cui fa riferimento un nome di chiave nel registro di sistema. Gli utenti possono assegnare i propri suoni agli avvisi e agli avvisi di sistema o alle azioni dell'utente, ad esempio un clic del pulsante del mouse. I suoni associati a avvisi di sistema e avvisi sono detti *eventi audio*.

Per riprodurre un evento audio, chiamare **PlaySound** con il parametro *pszSound* che punta a una stringa contenente il nome della voce del registro di sistema che identifica il suono. Ad esempio, per riprodurre il suono associato alla voce "click-through" e attendere il completamento del suono prima della restituzione, utilizzare l'istruzione seguente:


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



Se la voce del registro di sistema specificata o il file audio di forma d'onda identificato non esiste o se il file non rientra nella memoria disponibile, **PlaySound** riproduce il suono di sistema predefinito.

Gli eventi audio predefiniti dal sistema possono variare in base alla piattaforma. L'elenco seguente fornisce gli eventi audio definiti per tutte le implementazioni dell'API Win32:

-   SystemAsterisk
-   SystemExclamation
-   SystemExit
-   SystemHand
-   SystemQuestion
-   SystemStart

Se un'applicazione registra i propri eventi audio, l'utente può configurare l'evento audio usando l'interfaccia del pannello di controllo standard. L'applicazione deve registrare l'evento audio usando le funzioni del registro di sistema standard. Per ulteriori informazioni, vedere [Registro di sistema](../sysinfo/registry.md). Le voci appartengono alla stessa posizione della gerarchia del registro di sistema come il resto degli eventi audio. Questa posizione varia in base all'implementazione di Win32. Il valore di dati appropriato varia anche con l'implementazione di.

La funzione [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) cerca sempre nel registro di sistema un nome di chiave corrispondente a *lpszSound* prima di provare a caricare un file con questo nome. La funzione [**PlaySound**](/previous-versions//dd743680(v=vs.85)) accetta flag che specificano la posizione del suono.

 

 