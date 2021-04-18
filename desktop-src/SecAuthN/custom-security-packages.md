---
description: Viene illustrato come creare pacchetti di sicurezza personalizzati tramite l'API del pacchetto di sicurezza personalizzato.
ms.assetid: 915ef590-c427-4ac2-a2f7-aed328776cb7
title: Pacchetti di sicurezza personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4c447f1a24a3edc2f25a55f83d82c174094c50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308155"
---
# <a name="custom-security-packages"></a>Pacchetti di sicurezza personalizzati

Per implementare nuovi protocolli di sicurezza integrati con i sistemi operativi Windows Server e Windows, utilizzare l'API del pacchetto di sicurezza personalizzato e le funzioni dell' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA).

L'API del pacchetto di sicurezza personalizzato supporta lo sviluppo combinato di [*provider di supporto*](/windows/desktop/SecGloss/s-gly) per la sicurezza personalizzati, che forniscono servizi di [autenticazione non interattivi](noninteractive-authentication.md) e lo scambio di messaggi sicuro alle applicazioni client/server, con lo sviluppo di [*pacchetti di autenticazione*](/windows/desktop/SecGloss/a-gly)personalizzati, che forniscono servizi per le applicazioni che eseguono [l'autenticazione interattiva](interactive-authentication.md). Questi servizi, quando vengono combinati in un singolo pacchetto, sono detti pacchetto di Security Support Provider/autenticazione (SSP/AP).

Come per i pacchetti di sicurezza forniti da Microsoft, gli utenti del pacchetto di sicurezza personalizzato accedono ai servizi di autenticazione interattiva usando le [funzioni di accesso LSA](authentication-functions.md). È possibile accedere direttamente ai servizi di autenticazione e protezione dei messaggi non interattivi mediante SSPI ( [Security Support Provider Interface](sspi.md) ).

I pacchetti di sicurezza distribuiti in SSP/APs sono completamente integrati con LSA. Utilizzando le funzioni di supporto LSA disponibili per i pacchetti di sicurezza personalizzati, gli sviluppatori possono implementare funzionalità di sicurezza avanzate, ad esempio la creazione di token, il supporto [*supplementare delle credenziali*](/windows/desktop/SecGloss/s-gly) e l'autenticazione pass-through. Per un elenco di queste funzioni di supporto, vedere [funzioni LSA chiamate dai pacchetti di autenticazione](authentication-functions.md). Per informazioni su come implementare i pacchetti di sicurezza personalizzati, vedere [creazione di pacchetti di sicurezza personalizzati](creating-custom-security-packages.md).

Per ulteriori informazioni sui pacchetti di sicurezza personalizzati, vedere gli argomenti seguenti.



| Argomento                                                                                                                                                 | Descrizione                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [SSP/APs e SSP](ssp-aps-versus-ssps.md)<br/>                                                                                                | Informazioni su come determinare se un pacchetto di sicurezza deve trovarsi in un SSP/AP o SSP.<br/> |
| [Modalità LSA rispetto alla modalità utente](lsa-mode-versus-user-mode.md)<br/>                                                                                    | Informazioni dettagliate sulla modalità LSA e la modalità utente diverse.<br/>                                      |
| [Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza](restrictions-around-registering-and-installing-a-security-package.md)<br/> | Azioni per pacchetti di sicurezza non supportati in Windows.<br/>                              |



 

 

