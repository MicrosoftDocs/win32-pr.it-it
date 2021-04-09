---
title: Applicazioni DRM individualizzazione
description: Applicazioni DRM individualizzazione
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media Format SDK, applicazioni DRM individualizzazione
- Windows Media Format SDK, applicazione individualizzazione
- ASF (Advanced Systems Format), applicazioni DRM individualizzazione
- ASF (Advanced Systems Format), individualizzazione DRM Applications
- ASF (Advanced Systems Format), individualizzazione dell'applicazione
- ASF (Advanced Systems Format), individualizzazione applicazione
- Digital Rights Management (DRM), applicazioni individualizzazione
- DRM (Digital Rights Management), applicazioni individualizzazione
- Digital Rights Management (DRM), applicazione individualizzazione
- DRM (Digital Rights Management), individualizzazione dell'applicazione
- individualizzazione applicazione
- applicazioni DRM individualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "103956258"
---
# <a name="individualizing-drm-applications"></a>Applicazioni DRM individualizzazione

Per aumentare la sicurezza, il componente DRM delle applicazioni può essere *personalizzato*. Un'applicazione personalizzata è una che ha ricevuto un aggiornamento ai componenti DRM che lo differenzia da tutte le altre copie della stessa applicazione. I proprietari del contenuto possono richiedere che i file protetti vengano riprodotti solo in un'applicazione che è stata individualmente.

Il processo di individualizzazione viene avviato quando l'applicazione contatta il servizio di individualizzazione Microsoft, che quindi installa un aggiornamento della sicurezza nel computer dell'utente. Poiché il servizio di individualizzazione gestisce le informazioni dell'utente, è necessario visualizzare l'informativa sulla privacy di Microsoft o fornire un collegamento a tale pagina nel sito Web Microsoft: <https://privacy.microsoft.com/privacystatement> .

L'individualizzazione può essere eseguita in modi diversi. Ad esempio, l'individualizzazione può essere eseguita quando un utente riproduce un file protetto. La richiesta di licenza viene inviata al [*servizio Windows Media License*](wmformat-glossary.md), che controlla il certificato dell'applicazione che richiede la [*licenza*](wmformat-glossary.md). Se il componente DRM dell'applicazione non è stato individualizzato, il servizio licenze Windows Media rifiuta di emettere la licenza, perché si tratta dei criteri del servizio licenze Windows Media per emettere licenze solo per i giocatori individuali. L'applicazione può quindi notificare all'utente che l'applicazione deve essere aggiornata. Se l'utente acconsente, viene fornito un aggiornamento della sicurezza per individuare il componente DRM dell'applicazione.

Per migliorare l'esperienza utente, è possibile avviare il processo di individualizzazione come passaggio di aggiornamento della sicurezza durante l'installazione. l'utente non viene quindi interrotto per ottenere un aggiornamento della sicurezza durante il tentativo di riprodurre un file protetto. È anche possibile incoraggiare attivamente l'individualizzazione aggiungendo un comando o un pulsante di menu di **aggiornamento della sicurezza** all'applicazione.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 




