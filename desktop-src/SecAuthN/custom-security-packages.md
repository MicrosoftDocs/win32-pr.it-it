---
description: Viene illustrato come creare pacchetti di sicurezza personalizzati usando l'API del pacchetto di sicurezza personalizzato.
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: Pacchetti di sicurezza personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3799edb3eb8e0551afe7d7f7bcdc54924228445d6ffb28cb4773af843b5c2d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008669"
---
# <a name="custom-security-packages"></a>Pacchetti di sicurezza personalizzati

Per implementare nuovi protocolli di sicurezza integrati con i sistemi operativi Windows Server e Windows, usare l'API del pacchetto di sicurezza personalizzato e le funzioni LSA [*(Local Security Authority).*](/windows/desktop/SecGloss/l-gly)

L'API del pacchetto di sicurezza [](/windows/desktop/SecGloss/s-gly) personalizzato supporta lo sviluppo combinato di provider di supporto per la sicurezza (SSP) personalizzati, che forniscono servizi di autenticazione [non](noninteractive-authentication.md) interattiva e scambio di messaggi sicuro alle applicazioni client/server, con lo sviluppo di pacchetti di autenticazione [*personalizzati,*](/windows/desktop/SecGloss/a-gly)che forniscono servizi per le applicazioni che eseguono l'autenticazione [interattiva.](interactive-authentication.md) Questi servizi, se combinati in un singolo pacchetto, sono denominati provider di supporto per la sicurezza/pacchetto di autenticazione (SSP/AP).

Come per i pacchetti di sicurezza forniti da Microsoft, gli utenti dei pacchetti di sicurezza personalizzati accedono ai servizi di autenticazione interattiva usando le funzioni di accesso [LSA](authentication-functions.md). L'autenticazione non interattiva e i servizi di protezione dei messaggi sono accessibili direttamente tramite [Security Support Provider Interface](sspi.md) (SSPI).

I pacchetti di sicurezza distribuiti in SSP/APs sono completamente integrati con LSA. Usando le funzioni di supporto LSA disponibili per i pacchetti di sicurezza personalizzati, gli sviluppatori possono implementare funzionalità di sicurezza avanzate come la creazione di [*token,*](/windows/desktop/SecGloss/s-gly) il supporto delle credenziali supplementari e l'autenticazione pass-through. Per un elenco di queste funzioni di supporto, vedere [Funzioni LSA chiamate dai pacchetti di autenticazione](authentication-functions.md). Per informazioni su come implementare pacchetti di sicurezza personalizzati, vedere [Creazione di pacchetti di sicurezza personalizzati.](creating-custom-security-packages.md)

Per altre informazioni sui pacchetti di sicurezza personalizzati, vedere gli argomenti seguenti.



| Argomento                                                                                                                                                 | Descrizione                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Provider di servizi condivisi/provider di servizi condivisi e provider di servizi condivisi](ssp-aps-versus-ssps.md)<br/>                                                                                                | Informazioni su come determinare se un pacchetto di sicurezza deve essere in un provider di servizi condivisi o in un provider di servizi condivisi.<br/> |
| [Modalità LSA e modalità utente](lsa-mode-versus-user-mode.md)<br/>                                                                                    | Informazioni dettagliate sulle diverse modalità LSA e modalità utente.<br/>                                      |
| [Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza](restrictions-around-registering-and-installing-a-security-package.md)<br/> | Azioni da parte di pacchetti di sicurezza non supportati in Windows.<br/>                              |



 

 

