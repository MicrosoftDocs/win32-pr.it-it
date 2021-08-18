---
description: Per delegare le credenziali al protocollo CredSSP (Credential Security Support Provider Protocol), è necessario specificare a quali server è possibile delegare.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: CredSSP Criteri di gruppo Impostazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8efaaab1b49efba89c9fa5788f60df372991f388c474d531eff8f59205af441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008699"
---
# <a name="credssp-group-policy-settings"></a>CredSSP Criteri di gruppo Impostazioni

Per delegare le credenziali al protocollo [CredSSP (Credential Security Support Provider),](credential-security-support-provider.md) è necessario specificare a quali server è possibile delegare. Per specificare tali server, modificare le impostazioni nello snap-in Criteri di gruppo Editor Microsoft Management Console (MMC). Le impostazioni dell'oggetto Criteri di gruppo che controllano la delega sono in **Configurazione computer Modelli amministrativi delega delle credenziali di \| \| \| sistema**.

> [!Caution]  
> Non si tratta di delega vincolata. CredSSP passa le credenziali complete dell'utente al server senza alcun vincolo.

 

Le impostazioni di Criteri di gruppo controllano la delega dei tipi di credenziali seguenti.



| Tipo di credenziali                                                                                                                                 | Descrizione                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Credenziali predefinite<br/> | Le credenziali ottenute quando l'utente accede per la prima volta a Windows.<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Credenziali nuove<br/>         | Credenziali richieste dall'utente durante l'esecuzione di un'applicazione.<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Credenziali salvate<br/>         | Le credenziali salvate usando Gestione credenziali [.](credential-manager.md)<br/> |



 

Per includere un server nella categoria associata a [](/windows/desktop/SecGloss/s-gly) una determinata impostazione di Criteri di gruppo, aggiungere il nome dell'entità servizio (SPN) del server all'elenco di server per tale impostazione di Criteri di gruppo. Il nome SPN può contenere un singolo carattere jolly.

 

