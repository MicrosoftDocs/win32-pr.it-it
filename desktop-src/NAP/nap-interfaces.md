---
title: Interfacce NAP
description: Interfacce NAP
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff67fe21922c5b1baf9c2825dc7ea2852f14331
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045224"
---
# <a name="nap-interfaces"></a>Interfacce NAP

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il sistema NAP è costituito dalle interfacce seguenti.



| Interface Name (Nome interfaccia)                                                                   | Descrizione                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapCertRelyingParty**](inapcertrelyingparty.md)                             | Fornisce metodi che devono essere usati da certificati-relying party per comunicare con NapAgent.                                                        |
| [**INapClientManagement**](inapclientmanagement.md)                             | Utilizzato per la gestione client NAP della cache del rapporto di integrità e l'attivazione del rapporto di integrità. Deprecato.                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | Utilizzato per la gestione client NAP della cache del rapporto di integrità e l'attivazione del rapporto di integrità.                                                                            |
| [**INapComponentConfig**](inapcomponentconfig.md)                               | Utilizzato per la configurazione personalizzata dei componenti di convalida integrità di sistema. Deprecato.                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | Fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per configurare un'interfaccia utente di server dei criteri di rete in modalità remota.   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | Fornisce metodi di configurazione del sistema NAP per i validator di integrità di sistema (SHV) per impostare e modificare i dati di configurazione per un ID configurazione specifico. |
| [**INapComponentInfo**](inapcomponentinfo.md)                                   | Deve essere implementato dai componenti plug-in, ad esempio SHAs e SHV, in modo che possano essere comunicati con il sistema NAP.                          |
| [**INapEnforcementClientBinding**](inapenforcementclientbinding.md)             | Usato dai client di imposizione per comunicare con NapAgent.                                                                                       |
| [**INapEnforcementClientCallback**](inapenforcementclientcallback.md)           | I client di imposizione devono implementare questa interfaccia per consentire a NapAgent di comunicare con loro.                                                  |
| [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)       | Consente la gestione della connessione client. Deprecato.                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | Consente la gestione della connessione client.                                                                                                            |
| [**INapServerCallback**](inapservercallback.md)                                 | SHV utilizzare il metodo singolo su questa interfaccia per segnalare il completamento asincrono della richiesta.                                                             |
| [**INapServerInfo**](inapserverinfo.md)                                         | Utilizzato dai client di gestione (ad esempio provider WMI, strumenti da riga di comando e così via) per eseguire una query sullo stato del sistema server NAP.                             |
| [**INapServerManagement**](inapservermanagement.md)                             | Utilizzato per la gestione di base del server NAP.                                                                                                        |
| [**INapSoHConstructor**](inapsohconstructor.md)                                 | Usato da SHAs per creare richieste di rapporto di integrità e SHV per costruire risposte di rapporto di integrità.                                                                      |
| [**INapSoHProcessor**](inapsohprocessor.md)                                     | Usato da SHAs per elaborare il contenuto delle risposte a rapporto di integrità e di SHV per elaborare il contenuto delle richieste di rapporto di integrità.                                          |
| [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)             | SHAs deve usare questa interfaccia per comunicare con NapAgent. Deprecato.                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | SHAs deve usare questa interfaccia per comunicare con NapAgent.                                                                                      |
| [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)           | SHAs deve implementare questa interfaccia per coordinare l'elaborazione con il sistema NAP.                                                                    |
| [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)             | SHAs utilizzare questa interfaccia per comunicare e coordinare l'elaborazione con il sistema NAP.                                                         |
| [**INapSystemHealthValidator**](inapsystemhealthvalidator.md)                   | Fornisce metodi che devono essere implementati da un servizio di convalida integrità di sistema in modo che il sistema NAP possa comunicare con esso.                                                         |
| [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)   | SHV usare questa interfaccia per la comunicazione dei dati con la controparte lato client. Deprecato.                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | SHV usare questa interfaccia per la comunicazione dei dati con la controparte lato client.                                                                  |



 

 

 




