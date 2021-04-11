---
title: Individualizzazione DRM
description: Individualizzazione DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Media Format SDK, individualizzazione DRM
- Digital Rights Management (DRM), individualizzazione
- DRM (Digital Rights Management), individualizzazione
- individualizzazione di DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329148"
---
# <a name="drm-individualization"></a>Individualizzazione DRM

I proprietari di contenuti protetti possono richiedere agli utenti di aggiornare alcuni componenti di Digital Rights Management (DRM) inclusi in Windows Media Format SDK prima di accedere al contenuto. Se un utente accetta l'aggiornamento, una versione personalizzata di un file di protezione (uno univoco per il proprio computer) verrà scaricata da un sito Web Microsoft. Se l'utente rifiuta l'aggiornamento, non sarà in grado di accedere al contenuto; Tuttavia, saranno comunque in grado di accedere al contenuto non protetto e ai contenuti protetti che non richiedono l'aggiornamento. L'esecuzione di un aggiornamento della sicurezza consente di aumentare il livello di protezione offerto da DRM.

L'individualizzazione può essere eseguita in fase di installazione o quando un'applicazione rileva un file ASF protetto che la richiede. Poiché questo processo modifica i componenti di sistema di un utente, l'applicazione deve inviare una notifica all'utente e ottenere il consenso informato prima di eseguire l'aggiornamento. In Microsoft Windows Media Player, ad esempio, viene visualizzata una finestra di dialogo con il testo seguente:

**Aggiornamento della sicurezza obbligatorio**

**Il proprietario del contenuto protetto a cui si sta tentando di accedere richiede prima di tutto l'aggiornamento di alcuni componenti di Microsoft Digital Rights Management (DRM) nel computer.**

**Fare clic su OK per aggiornare i componenti di DRM.**

**Dettagli**

**Quando si fa clic su OK, un identificatore univoco e un file di protezione DRM vengono inviati a un servizio Microsoft su Internet. Il file viene sostituito con una versione personalizzata che contiene l'identificatore univoco. Questo aumenta il livello di protezione fornito da DRM.**

Qualsiasi applicazione che supporta l'individualizzazione deve usare la stessa formulazione o la stessa parola. Per ulteriori informazioni sull'informativa sulla privacy di Microsoft, vedere la sezione [informativa sulla privacy](privacy-statement.md) di questa documentazione.

> [!Note]  
> Il DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Applicazioni DRM individualizzazione**](individualizing-drm-applications.md)
</dt> </dl>

 

 




