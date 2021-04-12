---
description: Con la tecnologia di installazione tradizionale, è necessario uscire da un'applicazione ed eseguire di nuovo il programma di installazione per eseguire un'attività di installazione.
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: Installazione su richiesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f25c83135a0497d09aa0a7800a1272105d0db1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231870"
---
# <a name="installation-on-demand"></a>Installazione su richiesta

Con la tecnologia di installazione tradizionale, è necessario uscire da un'applicazione ed eseguire di nuovo il programma di installazione per eseguire un'attività di installazione. Questa situazione si verifica in genere quando un utente desidera una funzionalità o un prodotto non scelto durante la prima esecuzione del programma di installazione. Questa operazione rendeva spesso il processo di configurazione del prodotto inefficiente, perché richiedeva all'utente di prevedere le funzionalità necessarie prima di utilizzare il prodotto.

L'installazione su richiesta rende possibile offrire funzionalità a utenti e applicazioni in assenza dei file stessi. Questa nozione è nota come annuncio. Il Windows Installer ha la possibilità di annunciare la funzionalità e di rendere possibile l'installazione su richiesta di funzionalità dell'applicazione o di tutti i prodotti. Quando un utente o un'applicazione attiva una funzionalità o un prodotto pubblicizzato, il programma di installazione procede con l'installazione dei componenti necessari. In questo modo il processo di configurazione viene ridotto perché è possibile accedere a funzionalità aggiuntive senza dover uscire ed eseguire di nuovo un'altra procedura di installazione.

Quando un prodotto utilizza il programma di installazione, un utente può scegliere in fase di installazione le funzionalità o le applicazioni da installare e quali annunciare. Se durante l'esecuzione di un'applicazione l'utente richiede una funzionalità annunciata che non è ancora stata installata, l'applicazione chiama il programma di installazione per attuare un'installazione a livello di funzionalità JIT dei file necessari. Se l'utente attiva un prodotto annunciato che non è ancora stato installato, il sistema operativo chiama il programma di installazione per applicare un'installazione a livello di prodotto JIT.

L' [annuncio](advertisement.md) e l'installazione su richiesta possono anche semplificare la gestione del sistema consentendo agli amministratori di designare le applicazioni come richieste o facoltative per diversi gruppi di utenti. Esistono due tipi di annunci pubblicitari noti come "assegnazione" e "pubblicazione". Se un amministratore assegna un'applicazione a un gruppo, questi utenti possono installare l'applicazione su richiesta. Se, tuttavia, l'amministratore pubblica l'applicazione nel gruppo, nessun punto di ingresso appare a questi utenti e l'installazione su richiesta viene attivata solo se un'altra applicazione attiva l'applicazione pubblicata.

 

 



