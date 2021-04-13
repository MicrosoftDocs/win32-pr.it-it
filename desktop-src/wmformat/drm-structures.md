---
title: Strutture client DRM di Microsoft Windows Media
description: Strutture client DRM di Microsoft Windows Media
ms.assetid: 794de1b7-d60c-435e-9f77-c4df109b5372
keywords:
- Windows Media Format SDK, strutture
- Digital Rights Management (DRM), strutture
- DRM (Digital Rights Management), strutture
- API estese del client DRM, strutture
- API estese client, strutture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43264c37ed9830026f87998823017d17c9d75f7e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400084"
---
# <a name="microsoft-windows-media-drm-client-structures"></a>Strutture client DRM di Microsoft Windows Media

Le strutture seguenti sono supportate dalle API estese del client Windows Media DRM.



| Struttura o enumerazione                                                                    | Descrizione                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ID di \_ protezione dell'output audio \_ DRM \_**](drm-audio-output-protection-ids.md)              | Contiene un elenco di identificatori di protezione dell'output audio.                                                                                                     |
| [**\_ \_ \_ ID protezione output audio \_ DRM \_ es.**](drm-audio-output-protection-ids-ex.md)       | Contiene un elenco di identificatori di protezione dell'output audio. Questa struttura estende **gli \_ \_ \_ \_ ID protezione dell'output audio DRM** aggiungendo un numero di versione.          |
| [**\_copia DRM \_ OPL**](drmdrm-copy-opl.md)                                                   | Include informazioni sui livelli di protezione dell'output specificati in una licenza per le azioni di copia.                                                               |
| [**\_ \_ dati sullo stato della licenza DRM \_**](drmdrm-license-state-data.md)                              | Contiene informazioni sulle restrizioni di licenza per un diritto DRM.                                                                                        |
| [**\_livelli di \_ protezione dell'output minimo \_ DRM \_**](drmdrm-minimum-output-protection-levels.md) | Include i livelli minimi di protezione dell'output (OPLs) per la riproduzione di diversi tipi di contenuto.                                                                 |
| [**\_ \_ ID output OPL \_ DRM**](drmdrm-opl-output-ids.md)                                      | Include un numero di identificatori di output OPL.                                                                                                                   |
| [**\_protezione dell'output DRM \_**](drm-output-protection.md)                                    | Include informazioni su una tecnologia di protezione dell'output.                                                                                                    |
| [**protezione dell'output DRM, ad \_ \_ \_ esempio**](drm-output-protection-ex.md)                             | Include informazioni su una tecnologia di protezione dell'output. Questa struttura estende **la \_ \_ protezione dell'output DRM** aggiungendo un numero di versione.                     |
| [**\_riproduzione DRM \_ OPL**](drmdrm-play-opl.md)                                                   | Include informazioni sui OPLs specificati in una licenza per le azioni di riproduzione.                                                                                   |
| [**DRM \_ Play \_ OPL \_ ex**](drm-play-opl-ex.md)                                               | Include informazioni estese sui OPLs specificati in una licenza per le azioni di riproduzione.                                                                          |
| [**\_ID di \_ protezione dell'output del video DRM \_ \_**](drmdrm-video-output-protection-ids.md)           | Include una matrice di strutture di **\_ \_ \_ protezione dell'output video DRM** .                                                                                            |
| [**\_ \_ \_ ID protezione output video \_ DRM \_ es.**](drm-video-output-protection-ids-ex.md)       | Include una matrice di strutture di **\_ \_ \_ protezione dell'output video DRM** . Questa struttura estende **gli \_ \_ ID di \_ protezione \_ dell'output del video DRM** aggiungendo un numero di versione. |
| [**\_ \_ Stato ripristino del backup WM \_**](wm-backup-restore-status.md)                             | Include informazioni su un'operazione di backup o ripristino delle licenze in sospeso.                                                                                      |
| [**\_stato di personalizzazione WM \_**](drmwm-individualize-status.md)                             | Include informazioni su un processo di individualizzazione in sospeso.                                                                                                |
| [**\_restrizioni video analogiche WMDRM \_ \_**](wmdrm-analog-video-restrictions.md)               | Include informazioni su una restrizione per la riproduzione di contenuto come video analogo.                                                                             |
| [**\_ \_ restrizioni video ANALOGIche WMDRM \_ \_**](wmdrm-analog-video-restrictions-ex.md)        | Include informazioni estese su una restrizione per la riproduzione di contenuto come video analogo.                                                                    |
| [**\_blocco a \_ dispersione CRITTOGRAFAto WMDRM \_**](wmdrm-encrypt-scatter-block.md)                       | Contiene un blocco di dati da crittografare.                                                                                                                   |
| [**\_informazioni sulla \_ dispersione CRITTOGRAFAta WMDRM \_**](wmdrm-encrypt-scatter-info.md)                         | Contiene le informazioni necessarie per configurare l'interfaccia [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) per l'utilizzo.                                        |
| [**\_filtro licenze \_ WMDRM**](wmdrm-license-filter.md)                                      | Contiene informazioni di filtro per la creazione di enumerazioni delle licenze.                                                                                           |
| [**\_livelli di \_ protezione dell'output di WMDRM \_**](wmdrm-output-protection-levels.md)                 | Contiene i livelli di protezione dell'output richiesti da una licenza per eseguire varie azioni.                                                                    |
| [**WMDRMCryptoData**](wmdrmcryptodata.md)                                                  | Contiene informazioni sull'algoritmo di crittografia utilizzato per crittografare e decrittografare il contenuto.                                                                 |
| [**criteri di WMDRMNET \_**](wmdrmnet-policy.md)                                                 | Contiene i criteri da utilizzare per le operazioni di Windows Media DRM per i dispositivi di rete.                                                                        |
| [**\_ \_ requisiti globali del criterio WMDRMNET \_**](wmdrmnet-policy-global-requirements.md)       | Include i requisiti globali per Windows Media DRM per i dispositivi di rete.                                                                                        |
| [**\_ \_ ambiente minimo per i criteri WMDRMNET \_**](wmdrmnet-policy-minimum-environment.md)       | Contiene i requisiti di sicurezza minimi per Windows Media DRM per i dispositivi di rete.                                                                       |
| [**\_criteri WMDRMNET \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)                  | Include le informazioni sui criteri per la riproduzione di contenuto con Windows Media DRM per i dispositivi di rete.                                                               |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](drm-programming-reference.md)
</dt> </dl>

 

 




