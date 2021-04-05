---
description: I pacchetti di autenticazione sono contenuti nelle librerie a collegamento dinamico.
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: Pacchetti di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff02017b653521d80741bcdf3c205ab924c4bceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882665"
---
# <a name="authentication-packages"></a>Pacchetti di autenticazione

I [*pacchetti di autenticazione*](/windows/desktop/SecGloss/a-gly) sono contenuti nelle librerie a collegamento dinamico. L' [*autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) carica i pacchetti di autenticazione usando le informazioni di configurazione archiviate nel registro di sistema. Il caricamento di più pacchetti di autenticazione consente all'LSA di supportare più processi di accesso e più [*protocolli di sicurezza*](/windows/desktop/SecGloss/s-gly).

I processi di accesso utilizzano i pacchetti di autenticazione per analizzare i dati di accesso. I nuovi processi di accesso vengono aggiunti a un sistema aggiungendo un oggetto [*Gina*](/windows/desktop/SecGloss/g-gly) per raccogliere i dati di accesso necessari e, se necessario, aggiungendo un nuovo pacchetto di autenticazione per analizzare i dati.

I protocolli di sicurezza sono implementati dai pacchetti di autenticazione. Un pacchetto di autenticazione analizza i dati di accesso attenendosi alle regole e alle procedure stabilite in un protocollo di sicurezza.

I pacchetti di autenticazione sono responsabili delle attività seguenti:

-   Analisi dei dati di accesso per determinare se un' [*entità di sicurezza*](/windows/desktop/SecGloss/s-gly) può accedere a un sistema.
-   Creazione di una nuova [*sessione di accesso*](/windows/desktop/SecGloss/l-gly) e creazione di un identificatore di [*accesso*](/windows/desktop/SecGloss/l-gly) univoco per l'entità autenticata con esito positivo.
-   Passaggio delle informazioni di sicurezza all'LSA per il token di sicurezza dell'entità.

Quando un utente tenta un accesso interattivo, LSA chiama un pacchetto di autenticazione per determinare se consentire all'utente di accedere. MSV1 \_ 0, ad esempio, è un pacchetto di autenticazione installato con il sistema operativo Microsoft Windows. Il \_ pacchetto MSV1 0 accetta un nome utente e una password con [*hash*](/windows/desktop/SecGloss/h-gly) . Cerca il nome utente e la combinazione di password con hash nel database Gestione account di sicurezza (SAM). Se i dati di accesso corrispondono alle [*credenziali*](/windows/desktop/SecGloss/c-gly)archiviate, il pacchetto di autenticazione consente la riuscita dell'accesso.

Dopo aver autenticato le credenziali [*di un'entità di sicurezza*](/windows/desktop/SecGloss/s-gly) , un pacchetto di autenticazione è responsabile della creazione di una nuova sessione di accesso LSA per l'entità e dell'allocazione dell' [*identificatore di accesso*](/windows/desktop/SecGloss/l-gly) che identifica in modo univoco la sessione di accesso. Il pacchetto di autenticazione può associare le informazioni sulle credenziali alla sessione di accesso per le successive richieste di autenticazione. Ad esempio, il \_ pacchetto di autenticazione MSV1 0 (fornito da Microsoft) associa il nome dell'account utente e un hash della password dell'utente a ogni sessione di accesso.

Il pacchetto di autenticazione fornisce inoltre un set di [*identificatori di sicurezza*](/windows/desktop/SecGloss/s-gly) (SID) e altre informazioni appropriate per l'inclusione nel token di sicurezza creato dall'LSA. Questo token rappresenterà il [*contesto*](/windows/desktop/SecGloss/c-gly) di sicurezza dell'entità per l'accesso alle operazioni di Windows.

Dopo la creazione e l'associazione di una sessione di accesso a un'entità, le successive richieste di autenticazione effettuate per conto dell'entità vengono gestite in modo diverso rispetto all'accesso iniziale. Il pacchetto di autenticazione non crea una nuova sessione di accesso né restituisce informazioni per la creazione di un token. Il pacchetto di autenticazione può, tuttavia, associare le [*credenziali aggiuntive*](/windows/desktop/SecGloss/s-gly) ottenute durante un'autenticazione successiva con la sessione di accesso esistente dell'entità. Quando l'accesso a una risorsa richiesta richiede informazioni oltre le credenziali stabilite dall'accesso iniziale, vengono ottenute le credenziali aggiuntive. Ad esempio, quando un utente connesso richiede l'accesso alla rete Novell, è possibile chiamare un pacchetto di autenticazione specifico per Novell, che può essere autenticato e associato alla sessione di accesso. Queste credenziali possono essere usate come riferimento da un redirector Novell (tramite il pacchetto di autenticazione Novell) quando l'utente accede alla rete Novell.

Negli argomenti seguenti vengono illustrati i vari tipi di [*pacchetti di autenticazione*](/windows/desktop/SecGloss/a-gly):

-   [Pacchetti di autenticazione di Windows](windows-authentication-packages.md)
-   [Security Support Provider/pacchetti di autenticazione](security-support-provider-authentication-packages.md)
-   [Pacchetti di autenticazione forniti da Microsoft](authentication-packages-provided-by-microsoft.md)
-   [Pacchetti di sottoautenticazione](subauthentication-packages.md)

 

 
