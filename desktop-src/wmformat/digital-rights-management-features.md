---
title: Funzionalità di Rights Management digitali
description: Funzionalità di Rights Management digitali
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows Media Format SDK, funzionalità DRM
- Digital Rights Management (DRM), funzionalità
- DRM (Digital Rights Management), funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728010"
---
# <a name="digital-rights-management-features"></a>Funzionalità di Rights Management digitali

\[La funzionalità DRM di Windows Media è deprecata e non deve essere utilizzata. In alternativa, usare [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]

Digital Rights Management (DRM) è una tecnologia che i proprietari di contenuti possono usare per proteggere i file multimediali digitali mediante la relativa crittografia con una chiave, ovvero una porzione di dati che blocca e sblocca il contenuto. Per riprodurre un file ASF protetto, un consumer deve ottenere una licenza separata contenente la chiave. Ogni licenza contiene inoltre i diritti, determinati dal proprietario del contenuto o dall'emittente della licenza, che specificano come il consumer può utilizzare il file. Grazie alla tecnologia DRM, i proprietari dei contenuti possono fornire canzoni, video e altri file multimediali digitali tramite Internet in un formato di file protetto e controllare l'uso del contenuto digitale. La tecnologia Microsoft DRM è supportata anche da Windows Media Rights Manager, Windows Media Encoder e Windows Media Player. Per ulteriori informazioni generali sulla tecnologia DRM di Microsoft, visitare il [sito Web Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

Le sezioni seguenti illustrano le principali funzionalità correlate a DRM di Windows Media Format SDK.



| Sezione                                                                                            | Descrizione                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [Nozioni fondamentali su DRM](drm-basics.md)                                                                       | Viene fornita una breve panoramica della funzionalità DRM fornita da Windows Media Format SDK.                                         |
| [Versioni DRM](drm-versions.md)                                                                   | Descrive le principali differenze tra le versioni di protezione DRM disponibili per le applicazioni.                                     |
| [DRM Live](live-drm.md)                                                                           | Vengono descritti gli scenari resi possibili dalla protezione DRM "al volo".                                                                |
| [Individualizzazione DRM](drm-individualization.md)                                                 | Descrive l'aggiornamento della sicurezza dell'applicazione che può essere richiesto dai proprietari del contenuto DRM o dalle autorità emittenti di licenze.                                   |
| [Backup e ripristino di licenze DRM](backing-up-and-restoring-of-drm-licenses.md)           | Vengono descritti i vantaggi e gli svantaggi di consentire agli utenti di eseguire il backup e il ripristino delle licenze di contenuti.                                       |
| [Visualizzazione degli attributi DRM nell'editor di metadati](viewing-drm-attributes-in-the-metadata-editor.md) | Descrive le funzionalità di questo oggetto helper DRM e gli scenari in cui è stato progettato per supportare.                                   |
| [Livelli di protezione dell'output](output-protection-levels.md)                                           | Viene descritto in che modo i livelli di protezione dell'output rendono più flessibili le licenze DRM versione 10.                                                   |
| [Revoca delle licenze](license-revocation.md)                                                       | Descrive la revoca delle licenze.                                                                                                        |
| [Windows Media DRM 10 per i dispositivi di rete](windows-media-drm-10-for-network-devices.md)           | Introduce Windows Media DRM 10 per i dispositivi di rete e la relativa implementazione in questo SDK.                                              |
| [Percorso audio protetto Microsoft](microsoft-secure-audio-path--deprecated.md)                         | Viene descritta l'architettura Microsoft Secure Audio Path, che fornisce il livello massimo di protezione per il contenuto audio protetto. |
| [Masterizzazione playlist](playlist-burning.md)                                                           | Descrive la funzionalità di masterizzazione della playlist di DRM e il modo in cui è supportata in Windows Media Format SDK.                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> <dt>

[**Funzionalità**](features.md)
</dt> </dl>

 

 