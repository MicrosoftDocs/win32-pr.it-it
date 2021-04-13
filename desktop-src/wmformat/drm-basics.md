---
title: Nozioni fondamentali su DRM
description: Nozioni fondamentali su DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Media Format SDK, nozioni fondamentali su DRM
- Digital Rights Management (DRM), informazioni
- DRM (Digital Rights Management), informazioni
- Digital Rights Management (DRM), protezione del contenuto
- DRM (Digital Rights Management), protezione del contenuto
- Digital Rights Management (DRM), creazione di pacchetti di contenuto
- DRM (Digital Rights Management), contenuto del pacchetto
- Digital Rights Management (DRM), lettura di contenuto protetto
- DRM (Digital Rights Management), lettura di contenuto protetto
- protezione del contenuto
- creazione di pacchetti di contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396854"
---
# <a name="drm-basics"></a>Nozioni fondamentali su DRM

Le tecnologie DRM di Windows Media sono piuttosto semplici dal punto di vista di Windows Media Format SDK. I componenti dell'SDK possono essere usati per proteggere il contenuto e per riprodurre contenuti protetti.

## <a name="protecting-content"></a>Protezione del contenuto

La protezione del contenuto (detto anche contenuto del packaging) implica la crittografia della sezione di dati del file e include alcune informazioni nell'intestazione del file che consente ai giocatori di decrittografare il contenuto.

Per crittografare il contenuto, è necessaria una chiave, ovvero un valore utilizzato per il seeding degli algoritmi di crittografia. Una chiave è costituita da due parti: un valore di inizializzazione chiave (o chiave privata) e un identificatore di chiave (o chiave pubblica). Il valore di inizializzazione chiave è il valore Secret con cui si codifica il contenuto. L'identificatore di chiave è un valore pubblico incluso nell'intestazione di un file protetto.

Quando un file è protetto, non può essere decrittografato senza una licenza. Una licenza include informazioni che specificano le condizioni per l'utilizzo del contenuto protetto. Le condizioni di licenza vengono stabilite dal proprietario del contenuto e possono essere personalizzate per soddisfare diverse esigenze. Parte del processo di creazione del pacchetto di un file consiste nell'includere l'URL di una pagina Web in cui gli utenti possono acquisire una licenza per accedere al contenuto.

## <a name="reading-protected-content"></a>Lettura del contenuto protetto

Per leggere il contenuto protetto, una licenza per il contenuto deve risiedere nel computer client. Alcune restrizioni di licenza vengono controllate internamente dai componenti DRM di Windows Media Format SDK, mentre altre devono essere applicate dall'applicazione.

È possibile utilizzare gli oggetti di Windows Media Format SDK per consentire all'utente di acquisire licenze per il contenuto e di eseguire altre attività amministrative, ad esempio l'aggiornamento dei componenti DRM e il backup delle licenze.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




