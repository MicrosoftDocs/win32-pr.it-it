---
title: Individualizzazione di applicazioni DRM
description: Individualizzazione di applicazioni DRM
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media Format SDK, individualizzazione di applicazioni DRM
- Windows Media Format SDK, individualizzazione dell'applicazione
- Advanced Systems Format (ASF), individualizzazione di applicazioni DRM
- ASF (Advanced Systems Format), individualizzazione di applicazioni DRM
- Advanced Systems Format (ASF), individualizzazione delle applicazioni
- ASF (Advanced Systems Format), individualizzazione delle applicazioni
- digital rights management (DRM), individualizzazione delle applicazioni
- DRM (Digital Rights Management),individualizzazione delle applicazioni
- digital rights management (DRM), individualizzazione delle applicazioni
- DRM (Digital Rights Management),individualizzazione delle applicazioni
- individualizzazione dell'applicazione
- individualizzazione di applicazioni DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c57b6f884e2304508243180cc536899f991b1baab6f7f540f04f12fb805d6f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809021"
---
# <a name="individualizing-drm-applications"></a>Individualizzazione di applicazioni DRM

Per aumentare la sicurezza, il componente DRM delle applicazioni può *essere individualizzato.* Un'applicazione individualizzata è un'applicazione che ha ricevuto un aggiornamento ai componenti DRM che la differenzia da tutte le altre copie della stessa applicazione. I proprietari del contenuto possono richiedere che i file protetti siano riprodotti solo in un'applicazione che è stata individualizzata.

Il processo di individualizzazione viene avviato quando l'applicazione contatta il Servizio di individualizzazione Microsoft, che installa quindi un aggiornamento della sicurezza nel computer dell'utente. Poiché il servizio di individualizzazione gestisce le informazioni dell'utente, è necessario visualizzare l'informativa sulla privacy di Microsoft o fornire un collegamento a tale pagina nel sito Web Microsoft: <https://privacy.microsoft.com/privacystatement> .

La individualizzazione può essere eseguita in modi diversi. Ad esempio, la individualizzazione può verificarsi quando un utente riproduce un file protetto. La richiesta di licenza viene inviata al [*Windows Media License Service,*](wmformat-glossary.md)che controlla il certificato dell'applicazione che richiede la [*licenza*](wmformat-glossary.md). Se il componente DRM dell'applicazione non è stato individualizzato, Windows Media License Service rifiuta di rilasciare la licenza, perché è il criterio di Windows Media License Service rilasciare licenze solo ai lettori individualizzati. L'applicazione può quindi notificare all'utente che l'applicazione deve essere aggiornata. Se l'utente accetta, viene fornito un aggiornamento della sicurezza per individualizzare il componente DRM dell'applicazione.

Per una migliore esperienza utente, è possibile avviare il processo di individualizzazione come passaggio di aggiornamento della sicurezza durante l'installazione. l'utente non viene interrotto per ottenere un aggiornamento della sicurezza durante il tentativo di riprodurre un file protetto. È anche possibile incoraggiare attivamente l'individualizzazione aggiungendo un **pulsante** o un comando di menu Aggiornamento della sicurezza all'applicazione.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità Rights Management digital**](digital-rights-management-features.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




