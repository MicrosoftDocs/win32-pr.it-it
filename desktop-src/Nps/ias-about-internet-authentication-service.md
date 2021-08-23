---
title: Informazioni sulle estensioni di Server dei criteri di rete
description: Questa sezione descrive come implementare le DLL per estendere le funzionalità di Server dei criteri di rete. Descrive l'interazione tra Server dei criteri di rete e le DLL e presenta alcune considerazioni di progettazione relative alle DLL.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 204fff8d97548e79eed3e317b3e14291e7288b55c51384c25ef8b912ad2d6095
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799466"
---
# <a name="about-nps-extensions"></a>Informazioni sulle estensioni di Server dei criteri di rete

> [!Note]  
> Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete (NPS) a partire da Windows Server 2008. Il contenuto di questo argomento si applica sia a IAS che a Server dei criteri di rete. In tutto il testo, Server dei criteri di rete viene usato per fare riferimento a tutte le versioni del servizio, incluse le versioni originariamente denominate IAS.

 

Questa sezione descrive come implementare le DLL per estendere le funzionalità di Server dei criteri di rete. Descrive l'interazione tra Server dei criteri di rete e le DLL e presenta alcune considerazioni di progettazione relative alle DLL.

Server dei criteri di rete fornisce due punti di estensione, uno per l'autenticazione e l'altro per l'autorizzazione. L'autenticazione si riferisce alla verifica dell'identità dell'utente. L'autorizzazione si riferisce alla determinazione dei servizi che la rete deve fornire all'utente. I due punti di estensione corrispondono alle DLL dell'estensione di autenticazione e alle DLL dell'estensione di autorizzazione. Ogni punto di estensione può supportare più DLL.

Server dei criteri di rete fornisce sia servizi di autenticazione che di autorizzazione. Le DLL dell'estensione per l'autenticazione vengono chiamate da Server dei criteri di rete prima dell'autenticazione e dell'autorizzazione di Server dei criteri di rete predefiniti. Le DLL dell'estensione di autorizzazione vengono chiamate dopo l'autenticazione e l'autorizzazione di Server dei criteri di rete.

Il diagramma seguente illustra il flusso di pacchetti tramite un server RADIUS NPS espanso tramite DLL di estensione.

![Processo di autenticazione e autorizzazione nps](images/ias03.png)

Se una DLL dell'estensione di autenticazione restituisce ACCEPT, il pacchetto ignora l'autenticazione del server dei criteri di rete e passa direttamente all'autorizzazione NPS.

> [!Note]  
> Quando sono presenti più DLL di estensione di autenticazione, anche le altre DLL di estensione potrebbero essere ignorate. Per [altre informazioni, vedere Configurazione delle DLL di](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) estensione.

 

Se una DLL dell'estensione di autenticazione restituisce CONTINUE, il pacchetto passa all'autenticazione NPS e quindi all'autorizzazione NPS.

> [!Note]  
> Quando sono presenti più DLL dell'estensione di autenticazione, le altre DLL dell'estensione di autenticazione vengono richiamate prima dell'autenticazione di Server dei criteri di rete.

 

Gli argomenti seguenti descrivono le DLL di estensione in modo più dettagliato:

-   [Configurazione delle DLL di estensione](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [Chiamata delle DLL di estensione](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [Attributi di identificazione utente](/windows/desktop/Nps/ias-user-identification-attributes)

 

 