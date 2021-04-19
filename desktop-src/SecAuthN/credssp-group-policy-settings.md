---
description: Per il protocollo CredSSP (Credential Security Support Provider Protocol) per delegare le credenziali, è necessario specificare quali server possono essere delegati a.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Impostazioni Criteri di gruppo CredSSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313746"
---
# <a name="credssp-group-policy-settings"></a>Impostazioni Criteri di gruppo CredSSP

Per il [protocollo CredSSP (Credential Security Support Provider Protocol)](credential-security-support-provider.md) per delegare le credenziali, è necessario specificare quali server possono essere delegati a. Per specificare tali server, modificare le impostazioni nello snap-in di Editor Criteri di gruppo (GPE) di Microsoft Management Console (MMC). Le impostazioni GPE che controllano la delega sono in **Configurazione Computer \| modelli amministrativi \| \| delega credenziali di sistema**.

> [!Caution]  
> La delega non è vincolata. CredSSP passa le credenziali complete dell'utente al server senza vincoli.

 

Le impostazioni di criteri di gruppo controllano la delega dei tipi di credenziali seguenti.



| Tipo di credenziali                                                                                                                                 | Descrizione                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Credenziali predefinite<br/> | Credenziali ottenute quando l'utente accede per la prima volta a Windows.<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Credenziali aggiornate<br/>         | Credenziali richieste all'utente durante l'esecuzione di un'applicazione.<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Credenziali salvate<br/>         | Credenziali salvate mediante [Gestione credenziali](credential-manager.md).<br/> |



 

Per includere un server nella categoria associata a una particolare impostazione di criteri di gruppo, aggiungere il [*nome dell'entità servizio*](/windows/desktop/SecGloss/s-gly) (SPN) del server all'elenco dei server per l'impostazione di criteri di gruppo. Il nome SPN può contenere un singolo carattere jolly.

 

