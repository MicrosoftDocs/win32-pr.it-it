---
title: Interfacce di Protezione accesso alla rete
description: Interfacce di Protezione accesso alla rete
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b704e8924886047b0a50aef7929f52be276a0417d118f2026e47706f95678a2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620820"
---
# <a name="nap-interfaces"></a>Interfacce di Protezione accesso alla rete

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il sistema di Protezione accesso alla rete è costituito dalle interfacce seguenti.



| Interface Name (Nome interfaccia)                                                                   | Descrizione                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapCertRelyingParty**](inapcertrelyingparty.md)                             | Fornisce metodi che le relying party di certificati devono utilizzare per comunicare con NapAgent.                                                        |
| [**INapClientManagement**](inapclientmanagement.md)                             | Usato per la gestione client di Protezione accesso alla rete della cache SoH e dell'attivazione dello scambio SoH. Deprecato.                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | Usato per la gestione client di Protezione accesso alla rete della cache SoH e dell'attivazione dello scambio SoH.                                                                            |
| [**INapComponentConfig**](inapcomponentconfig.md)                               | Usato per la configurazione personalizzata dei componenti SHV. Deprecato.                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | Fornisce metodi di configurazione di sistema di Protezione accesso alla rete per i validator dell'integrità del sistema per configurare un'interfaccia utente del server dei criteri di rete in modalità remota.   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | Fornisce metodi di configurazione di sistema di Protezione accesso alla rete per i validator di integrità del sistema per impostare e modificare i dati di configurazione per un ID di configurazione specifico. |
| [**INapComponentInfo**](inapcomponentinfo.md)                                   | Deve essere implementato dai componenti plug-in, ad esempio SHA e SHV, in modo che possano essere comunicati con il sistema di Protezione accesso alla rete.                          |
| [**INapEnforcementClientBinding**](inapenforcementclientbinding.md)             | Utilizzato dai client di imposizione per comunicare con NapAgent.                                                                                       |
| [**INapEnforcementClientCallback**](inapenforcementclientcallback.md)           | I client di imposizione devono implementare questa interfaccia per consentire a NapAgent di comunicare con essi.                                                  |
| [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)       | Consente la gestione delle connessioni client. Deprecato.                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | Consente la gestione delle connessioni client.                                                                                                            |
| [**INapServerCallback**](inapservercallback.md)                                 | Gli SHV usano il singolo metodo su questa interfaccia per segnalare il completamento della richiesta asincrona.                                                             |
| [**INapServerInfo**](inapserverinfo.md)                                         | Usato dai client di gestione ,ad esempio provider WMI, strumenti da riga di comando e così via, per eseguire query sullo stato del sistema server protezione accesso alla rete.                             |
| [**INapServerManagement**](inapservermanagement.md)                             | Utilizzato per la gestione di base del server protezione accesso alla rete.                                                                                                        |
| [**INapSoHConstructor**](inapsohconstructor.md)                                 | Usato da SHAs per costruire richieste SoH e da SHV per costruire SoH-responses.                                                                      |
| [**INapSoHProcessor**](inapsohprocessor.md)                                     | Usato dalle sha per elaborare il contenuto delle risposte SoH e da SHV per elaborare il contenuto delle richieste SoH.                                          |
| [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)             | Gli SHA devono usare questa interfaccia per comunicare con NapAgent. Deprecato.                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | Gli SHA devono usare questa interfaccia per comunicare con NapAgent.                                                                                      |
| [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)           | Gli sha devono implementare questa interfaccia per coordinare l'elaborazione con il sistema nap.                                                                    |
| [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)             | Gli sha usano questa interfaccia per comunicare e coordinarne l'elaborazione con il sistema di Protezione accesso alla rete.                                                         |
| [**INapSystemHealthValidator**](inapsystemhealthvalidator.md)                   | Fornisce metodi che un shv deve implementare in modo che il sistema di Protezione accesso alla rete possa comunicare con esso.                                                         |
| [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)   | Gli SHV usano questa interfaccia per la comunicazione dei dati con la controparte lato client. Deprecato.                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | Gli SHV usano questa interfaccia per la comunicazione dei dati con la controparte lato client.                                                                  |



 

 

 




