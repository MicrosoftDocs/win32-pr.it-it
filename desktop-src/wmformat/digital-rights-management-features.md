---
title: Funzionalità Rights Management digital
description: Funzionalità Rights Management digital
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows Media Format SDK, funzionalità DRM
- digital rights management (DRM), funzionalità
- DRM (Digital Rights Management),funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e389efdbfd3edef3f3c881cab8482c8ed03b6bb09eb4a7773caa59b4b9b1ad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118704870"
---
# <a name="digital-rights-management-features"></a>Funzionalità Rights Management digital

\[La Windows Media DRM è deprecata e non deve essere usata. Usare [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) in alternativa.\]

DRM (Digital Rights Management) è una tecnologia che i proprietari di contenuti possono usare per proteggere i file multimediali digitali crittografandoli con una chiave ( un dato che blocca e sblocca il contenuto). Per riprodurre un file ASF protetto, un consumer deve ottenere una licenza separata contenente la chiave. Ogni licenza contiene anche i diritti, determinati dal proprietario del contenuto o dall'emittente della licenza, che specificano come l'utente può usare il file. Usando la tecnologia DRM, i proprietari di contenuti possono distribuire tracce, video e altri file multimediali digitali su Internet in un formato di file protetto e controllare l'uso del contenuto digitale. La tecnologia Microsoft DRM è supportata anche da Windows Media Rights Manager, Windows Media Encoder e Windows Media Player. Per altre informazioni di base sulla tecnologia DRM di Microsoft, vedere il sito Web [microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

Le sezioni seguenti illustrano le principali funzionalità correlate a DRM di Windows Media Format SDK.



| Sezione                                                                                            | Descrizione                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Nozioni di base su DRM](drm-basics.md)                                                                       | Fornisce una breve panoramica della funzionalità DRM fornita da Windows Media Format SDK.                                         |
| [Versioni DRM](drm-versions.md)                                                                   | Descrive le differenze principali tra le versioni della protezione DRM disponibili per le applicazioni.                                     |
| [Live DRM](live-drm.md)                                                                           | Descrive gli scenari resi possibili dalla protezione DRM "in tempo reale".                                                                |
| [Individualizzazione DRM](drm-individualization.md)                                                 | Descrive l'aggiornamento della sicurezza delle applicazioni che i proprietari di contenuto DRM o gli emittente di licenze possono richiedere.                                   |
| [Backup e ripristino di licenze DRM](backing-up-and-restoring-of-drm-licenses.md)           | Descrive i vantaggi e gli vantaggi dell'autorizzazione degli utenti a eseguire il backup e il ripristino delle licenze per il contenuto.                                       |
| [Visualizzazione degli attributi DRM nell'editor dei metadati](viewing-drm-attributes-in-the-metadata-editor.md) | Descrive le funzionalità di questo oggetto helper DRM e gli scenari che è stato progettato per supportare.                                   |
| [Livelli di protezione dell'output](output-protection-levels.md)                                           | Descrive in che modo i livelli di protezione dell'output rendono le licenze DRM versione 10 più flessibili.                                                   |
| [Revoca delle licenze](license-revocation.md)                                                       | Descrive la revoca delle licenze.                                                                                                        |
| [Windows Media DRM 10 per dispositivi di rete](windows-media-drm-10-for-network-devices.md)           | Introduce Windows Media DRM 10 per dispositivi di rete e la relativa implementazione in questo SDK.                                              |
| [Percorso audio sicuro Microsoft](microsoft-secure-audio-path--deprecated.md)                         | Descrive l'architettura Microsoft Secure Audio Path, che offre il massimo livello di protezione per il contenuto audio protetto. |
| [Playlist Disasserta](playlist-burning.md)                                                           | Descrive la funzionalità di riproduzione delle playlist di DRM e come è supportata in Windows Media Format SDK.                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Funzionalità**](features.md)
</dt> </dl>

 

 