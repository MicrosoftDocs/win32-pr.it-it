---
description: Viene illustrato il modello di autenticazione LSA.
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: Modello di autenticazione LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27f5a44a20284a7285eb7fcffe1d1f8f6bf1f286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315875"
---
# <a name="lsa-authentication-model"></a>Modello di autenticazione LSA

Il modello di autenticazione LSA ( [*Local Security Authority*](../secgloss/l-gly.md) ) presenta le funzionalità seguenti:

-   L'autenticazione LSA supporta i [pacchetti di autenticazione](authentication-packages.md)personalizzati. In questo modo, i clienti finali e i fornitori di software indipendenti (ISV) possono personalizzare o sostituire le routine di autenticazione per soddisfare i requisiti oltre a quelli forniti dai pacchetti di autenticazione Microsoft standard. Mentre i pacchetti di autenticazione forniti da Microsoft richiedono un nome utente e i dati di accesso alla password, un pacchetto di autenticazione personalizzato può assumere altre forme di dati di accesso, ad esempio le informazioni sulla carta ATM e un PIN (Personal Identification Number). Un pacchetto di autenticazione personalizzato può essere utilizzato anche per implementare un nuovo [*protocollo di sicurezza*](../secgloss/s-gly.md).
-   LSA supporta i pacchetti di sicurezza personalizzati, che funzionano come provider di supporto della sicurezza per le applicazioni distribuite e come pacchetti di autenticazione per le applicazioni che richiedono servizi di autenticazione. È possibile accedere alla funzionalità di autenticazione utilizzando la stessa interfaccia di un pacchetto di autenticazione autonomo, mentre è possibile accedere alla funzionalità di Security Support Provider mediante SSPI ( [Security Support Provider Interface](sspi.md) ). Il set di funzioni di supporto LSA disponibili per i pacchetti di sicurezza personalizzati consente loro di fornire funzionalità di sicurezza avanzate, ad esempio la creazione di token e la gestione delle [*credenziali supplementari*](../secgloss/s-gly.md) .
-   LSA supporta la gestione di credenziali eterogenee per l'interfaccia con prodotti non Microsoft, ad esempio reti e database. Poiché questi prodotti hanno spesso le proprie credenziali di sicurezza, LSA fornisce funzioni che i pacchetti di autenticazione possono usare per associare le credenziali non Microsoft ai processi di Windows. I pacchetti di autenticazione personalizzati possono fornire servizi per l'esecuzione di query su queste credenziali quando necessario, ad esempio quando un redirector di rete tenta di stabilire una connessione a un sistema remoto.
-   Ogni classe di dispositivo di accesso installato in un sistema può avere un proprio processo di accesso. Le classi di dispositivi includono in genere dispositivi come i lettori di smart card; Tuttavia, ai fini dell'autenticazione [*LSA*](../secgloss/l-gly.md) , le reti connesse vengono considerate anche come dispositivi. Per impostazione predefinita, il sistema operativo Windows fornisce il processo di accesso che supporta gli accessi a nome utente e password tramite una tastiera. Gli sviluppatori possono aggiungere il supporto per altri dispositivi, ad esempio i [*lettori*](../secgloss/r-gly.md)di [*Smart Card*](../secgloss/s-gly.md) . Per ulteriori informazioni sulle smart card, vedere [autenticazione con smart card](smart-card-authentication.md). Per ulteriori informazioni sul supporto dei dispositivi di accesso, vedere [Winlogon e Gina](winlogon-and-gina.md).

 

 
