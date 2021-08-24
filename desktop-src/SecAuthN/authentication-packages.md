---
description: I pacchetti di autenticazione sono contenuti in librerie a collegamento dinamico.
ms.assetid: b0d7bca1-b4bb-4b3f-822e-04a6a500cd9a
title: Pacchetti di autenticazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d556489d520ebf45224e3e9b8a5526cc4debcf1c7e7ab95028ecd9e35a6de217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141364"
---
# <a name="authentication-packages"></a>Pacchetti di autenticazione

[*I pacchetti di*](/windows/desktop/SecGloss/a-gly) autenticazione sono contenuti in librerie a collegamento dinamico. [*L'autorità di sicurezza locale*](/windows/desktop/SecGloss/l-gly) (LSA) carica i pacchetti di autenticazione usando le informazioni di configurazione archiviate nel Registro di sistema. Il caricamento di più pacchetti di autenticazione consente all'LSA di supportare più processi di accesso e più [*protocolli di sicurezza.*](/windows/desktop/SecGloss/s-gly)

I processi di accesso usano i pacchetti di autenticazione per analizzare i dati di accesso. I nuovi processi di accesso vengono aggiunti a un sistema aggiungendo [*un'analisi DELL'accesso*](/windows/desktop/SecGloss/g-gly) per raccogliere i dati di accesso necessari e, se necessario, mediante l'aggiunta di un nuovo pacchetto di autenticazione per analizzare i dati.

I protocolli di sicurezza vengono implementati dai pacchetti di autenticazione. Un pacchetto di autenticazione analizza i dati di accesso seguendo le regole e le procedure impostate in un protocollo di sicurezza.

I pacchetti di autenticazione sono responsabili delle attività seguenti:

-   Analisi dei dati di accesso per determinare se a [*un'entità di*](/windows/desktop/SecGloss/s-gly) sicurezza è consentito l'accesso a un sistema.
-   Stabilire una nuova sessione [*di accesso e creare*](/windows/desktop/SecGloss/l-gly) un identificatore di accesso [*univoco*](/windows/desktop/SecGloss/l-gly) per l'entità autenticata correttamente.
-   Passaggio delle informazioni di sicurezza all'LSA per il token di sicurezza dell'entità.

Quando un utente tenta un accesso interattivo, l'account LSA chiama un pacchetto di autenticazione per determinare se consentire all'utente di accedere. MSV1 \_ 0, ad esempio, è un pacchetto di autenticazione installato con il sistema operativo microsoft Windows. Il pacchetto MSV1 \_ 0 accetta un nome utente e una [*password con hash.*](/windows/desktop/SecGloss/h-gly) Cerca la combinazione di nome utente e password con hash nel database di Gestione account di sicurezza (SAM). Se i dati di accesso corrispondono alle [*credenziali archiviate,*](/windows/desktop/SecGloss/c-gly)il pacchetto di autenticazione consente l'esito positivo dell'accesso.

Dopo aver autenticato correttamente le credenziali di un'entità di sicurezza, un pacchetto di autenticazione è [](/windows/desktop/SecGloss/l-gly) responsabile della creazione di una nuova sessione di accesso LSA per [*l'entità e dell'allocazione dell'identificatore*](/windows/desktop/SecGloss/s-gly) di accesso che identifica in modo univoco la sessione di accesso. Il pacchetto di autenticazione può associare le informazioni sulle credenziali alla sessione di accesso per le richieste di autenticazione successive. Ad esempio, il pacchetto di autenticazione MSV1 0 (fornito da Microsoft) associa il nome dell'account utente e un hash della \_ password dell'utente a ogni sessione di accesso.

Il pacchetto di autenticazione [](/windows/desktop/SecGloss/s-gly) fornisce anche un set di ID di sicurezza (SID) e altre informazioni appropriate per l'inclusione nel token di sicurezza creato dall'LSA. Questo token rappresenterà il contesto di sicurezza dell'entità [*per*](/windows/desktop/SecGloss/c-gly) l'accesso Windows operazioni.

Dopo che una sessione di accesso è stata creata e associata a un'entità, le successive richieste di autenticazione effettuate per conto dell'entità vengono gestite in modo diverso rispetto all'accesso iniziale. Il pacchetto di autenticazione non crea una nuova sessione di accesso né restituisce informazioni per la creazione di un token. Il pacchetto di autenticazione può tuttavia associare le [*credenziali supplementari ottenute*](/windows/desktop/SecGloss/s-gly) durante un'autenticazione successiva alla sessione di accesso esistente dell'entità. Le credenziali supplementari vengono ottenute quando l'accesso a una risorsa richiesta richiede informazioni che non superano le credenziali stabilite dall'accesso iniziale. Ad esempio, quando un utente connesso richiede un accesso alla rete Novell, è possibile chiamare un pacchetto di autenticazione specifico di Novell e le credenziali specifiche di Novell possono essere autenticate e associate alla sessione di accesso. È possibile fare riferimento a queste credenziali da un redirector Novell (tramite il pacchetto di autenticazione Novell) quando l'utente accede alla rete Novell.

Gli argomenti seguenti illustrano i vari tipi di pacchetti [*di autenticazione*](/windows/desktop/SecGloss/a-gly):

-   [Windows Pacchetti di autenticazione](windows-authentication-packages.md)
-   [Provider di supporto per la sicurezza/Pacchetti di autenticazione](security-support-provider-authentication-packages.md)
-   [Pacchetti di autenticazione forniti da Microsoft](authentication-packages-provided-by-microsoft.md)
-   [Pacchetti di sottoautenticazione](subauthentication-packages.md)

 

 
