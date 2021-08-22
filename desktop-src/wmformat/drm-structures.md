---
title: Strutture client di Microsoft Windows Media DRM
description: Strutture client di Microsoft Windows Media DRM
ms.assetid: 794de1b7-d60c-435e-9f77-c4df109b5372
keywords:
- Windows MEDIA Format SDK, strutture
- digital rights management (DRM), strutture
- DRM (digital rights management), strutture
- API estese del client DRM, strutture
- API estese client, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 145381cc6d702dd338176ffa89983de137285dcd7aef946d3ece956eb450880c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447841"
---
# <a name="microsoft-windows-media-drm-client-structures"></a>Strutture client di Microsoft Windows Media DRM

Le strutture seguenti sono supportate dalle API estese del client DRM Windows media.



| Struttura o enumerazione                                                                    | Descrizione                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID PROTEZIONE \_ OUTPUT AUDIO \_ \_ \_ DRM**](drm-audio-output-protection-ids.md)              | Contiene un elenco di identificatori di protezione dell'output audio.                                                                                                     |
| [**DRM \_ AUDIO \_ OUTPUT \_ PROTECTION \_ IDS \_ EX**](drm-audio-output-protection-ids-ex.md)       | Contiene un elenco di identificatori di protezione dell'output audio. Questa struttura estende **DRM \_ AUDIO OUTPUT \_ PROTECTION \_ \_ IDS** aggiungendo un numero di versione.          |
| [**DRM \_ COPY \_ OPL**](drmdrm-copy-opl.md)                                                   | Contiene informazioni sui livelli di protezione dell'output specificati in una licenza per le azioni di copia.                                                               |
| [**DATI SULLO STATO \_ DELLA \_ LICENZA \_ DRM**](drmdrm-license-state-data.md)                              | Contiene informazioni sulle restrizioni di licenza per un diritto DRM.                                                                                        |
| [**LIVELLI MINIMI \_ DI \_ PROTEZIONE \_ DELL'OUTPUT \_ DRM**](drmdrm-minimum-output-protection-levels.md) | Contiene i livelli minimi di protezione dell'output (OPL) per la riproduzione di vari tipi di contenuto.                                                                 |
| [**ID \_ DI OUTPUT OPL DRM \_ \_**](drmdrm-opl-output-ids.md)                                      | Contiene diversi identificatori di output OPL.                                                                                                                   |
| [**PROTEZIONE \_ DELL'OUTPUT \_ DRM**](drm-output-protection.md)                                    | Contiene informazioni su una tecnologia di protezione dell'output.                                                                                                    |
| [**PROTEZIONE \_ DELL'OUTPUT DRM \_ \_ EX**](drm-output-protection-ex.md)                             | Contiene informazioni su una tecnologia di protezione dell'output. Questa struttura estende **DRM \_ OUTPUT \_ PROTECTION** aggiungendo un numero di versione.                     |
| [**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)                                                   | Contiene informazioni sugli OPL specificati in una licenza per le azioni di riproduzione.                                                                                   |
| [**DRM \_ PLAY \_ OPL \_ EX**](drm-play-opl-ex.md)                                               | Contiene informazioni estese sugli OPL specificati in una licenza per le azioni di riproduzione.                                                                          |
| [**ID DI \_ PROTEZIONE \_ DELL'OUTPUT VIDEO \_ \_ DRM**](drmdrm-video-output-protection-ids.md)           | Contiene una matrice di **strutture DRM \_ VIDEO OUTPUT \_ \_ PROTECTION.**                                                                                            |
| [**ID DI \_ PROTEZIONE DELL'OUTPUT VIDEO DRM \_ \_ \_ \_ EX**](drm-video-output-protection-ids-ex.md)       | Contiene una matrice di **strutture DRM \_ VIDEO OUTPUT \_ \_ PROTECTION.** Questa struttura estende **DRM \_ VIDEO OUTPUT \_ PROTECTION \_ \_ IDS** aggiungendo un numero di versione. |
| [**STATO \_ RIPRISTINO \_ BACKUP WM \_**](wm-backup-restore-status.md)                             | Contiene informazioni su un'operazione di backup o ripristino delle licenze in sospeso.                                                                                      |
| [**WM \_ INDIVIDUALIZE \_ STATUS**](drmwm-individualize-status.md)                             | Contiene informazioni su un processo di individualizzazione in sospeso.                                                                                                |
| [**RESTRIZIONI VIDEO \_ ANALOGICHE \_ WMDRM \_**](wmdrm-analog-video-restrictions.md)               | Contiene informazioni su una restrizione per la riproduzione di contenuto come video analogico.                                                                             |
| [**RESTRIZIONI VIDEO ANALOGICHE WMDRM \_ \_ \_ \_ EX**](wmdrm-analog-video-restrictions-ex.md)        | Contiene informazioni estese su una restrizione per la riproduzione di contenuto come video analogico.                                                                    |
| [**BLOCCO A \_ DISPERSIONE WMDRM ENCRYPT \_ \_**](wmdrm-encrypt-scatter-block.md)                       | Contiene un blocco di dati da crittografare.                                                                                                                   |
| [**WMDRM \_ ENCRYPT SCATTER INFO (CRITTOGRAFARE LE INFORMAZIONI SULLA \_ \_ DISPERSIONE)**](wmdrm-encrypt-scatter-info.md)                         | Contiene le informazioni necessarie per configurare [**l'interfaccia IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) per l'uso.                                        |
| [**FILTRO LICENZE \_ \_ WMDRM**](wmdrm-license-filter.md)                                      | Contiene informazioni di filtro per la creazione di enumerazioni di licenze.                                                                                           |
| [**LIVELLI DI PROTEZIONE \_ DELL'OUTPUT \_ \_ WMDRM**](wmdrm-output-protection-levels.md)                 | Contiene i livelli di protezione dell'output richiesti da una licenza per eseguire varie azioni.                                                                    |
| [**WMDRMCryptoData**](wmdrmcryptodata.md)                                                  | Contiene informazioni sull'algoritmo di crittografia usato per crittografare e decrittografare il contenuto.                                                                 |
| [**CRITERI WMDRMNET \_**](wmdrmnet-policy.md)                                                 | Contiene i criteri da usare per l'Windows DRM multimediale per le operazioni dei dispositivi di rete.                                                                        |
| [**REQUISITI GLOBALI DEI CRITERI WMDRMNET \_ \_ \_**](wmdrmnet-policy-global-requirements.md)       | Contiene i requisiti globali per Windows DRM multimediale per i dispositivi di rete.                                                                                        |
| [**AMBIENTE MINIMO DEI CRITERI WMDRMNET \_ \_ \_**](wmdrmnet-policy-minimum-environment.md)       | Contiene i requisiti minimi di sicurezza per Windows DRM multimediale per i dispositivi di rete.                                                                       |
| [**TRANSCRYPTPLAY \_ DEI CRITERI \_ WMDRMNET**](wmdrmnet-policy-transcryptplay.md)                  | Contiene le informazioni sui criteri per la riproduzione di contenuto usando Windows Media DRM per dispositivi di rete.                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](drm-programming-reference.md)
</dt> </dl>

 

 




