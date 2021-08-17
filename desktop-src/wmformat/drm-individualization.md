---
title: Individualizzazione DRM
description: Individualizzazione DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Media Format SDK, individualizzazione DRM
- digital rights management (DRM), individualizzazione
- DRM (digital rights management), individualizzazione
- individualizzazione di DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16704c968002ee9d9d9cd9a47bf71dd315c2c599848b2ea18b23408ec7a0507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848692"
---
# <a name="drm-individualization"></a>Individualizzazione DRM

I proprietari di contenuto protetto possono richiedere agli utenti di aggiornare alcuni dei componenti DRM (Digital Rights Management) inclusi in Windows Media Format SDK prima di accedere al contenuto. Se un utente accetta l'aggiornamento, una versione individualizzata di un file di sicurezza (univoco per il computer) verrà scaricata da un sito Web Microsoft. Se l'utente rifiuta l'aggiornamento, non sarà in grado di accedere al contenuto. Tuttavia, potranno comunque accedere a contenuto non protetto e a contenuto protetto che non richiede l'aggiornamento. L'esecuzione di un aggiornamento della sicurezza consente di aumentare il livello di protezione offerto da DRM.

L'individualizzazione può essere eseguita in fase di installazione o quando un'applicazione rileva per la prima volta un file ASF protetto che lo richiede. Poiché questo processo modifica i componenti di sistema di un utente, l'applicazione deve inviare una notifica all'utente e ottenere il consenso informato prima di eseguire l'aggiornamento. Microsoft Windows Media Player, ad esempio, mostra una finestra di dialogo con il testo seguente:

**Aggiornamento della sicurezza obbligatorio**

**Il proprietario del contenuto protetto a cui si sta tentando di accedere richiede prima di tutto di aggiornare alcuni componenti di Microsoft Digital Rights Management (DRM) nel computer.**

**Fare clic su OK per aggiornare i componenti DRM.**

**Dettagli:**

**Quando si fa clic su OK, un identificatore univoco e un file di sicurezza DRM vengono inviati a un servizio Microsoft su Internet. Il file viene sostituito con una versione personalizzata che contiene l'identificatore univoco. Ciò aumenta il livello di protezione fornito da DRM.**

Qualsiasi applicazione che supporta l'individualizzazione deve usare la stessa formulazione o una formulazione simile. Per altre informazioni sull'Informativa sulla privacy di Microsoft, vedere la sezione Informativa sulla [privacy](privacy-statement.md) di questa documentazione.

> [!Note]  
> DRM non è supportato dalla versione basata su x64 di questo SDK.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità Rights Management digitali**](digital-rights-management-features.md)
</dt> <dt>

[**Individualizzazione delle applicazioni DRM**](individualizing-drm-applications.md)
</dt> </dl>

 

 




