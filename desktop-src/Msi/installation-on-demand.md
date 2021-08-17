---
description: Con la tecnologia di installazione tradizionale, è necessario uscire da un'applicazione ed eseguire nuovamente il programma di installazione per eseguire un'attività di installazione.
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: Installazione su richiesta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd20f83465fa110c4f749c6f11ba5ece1c6797a521174a8caebb9d152740aaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633870"
---
# <a name="installation-on-demand"></a>Installazione su richiesta

Con la tecnologia di installazione tradizionale, è necessario uscire da un'applicazione ed eseguire nuovamente il programma di installazione per eseguire un'attività di installazione. Questo errore si verifica in genere quando un utente vuole che una funzionalità o un prodotto non sia stato scelto durante la prima esecuzione dell'installazione. Questo spesso ha reso inefficiente il processo di configurazione del prodotto perché richiedeva all'utente di prevedere le funzionalità necessarie prima di usare il prodotto.

L'installazione su richiesta consente di offrire funzionalità a utenti e applicazioni in assenza dei file stessi. Questa nozione è nota come annuncio pubblicitario. Il Windows installer offre funzionalità di pubblicità e rende possibile l'installazione su richiesta di funzionalità dell'applicazione o di interi prodotti. Quando un utente o un'applicazione attiva una funzionalità o un prodotto annunciato, il programma di installazione procede con l'installazione dei componenti necessari. In questo modo si riduce il processo di configurazione perché è possibile accedere a funzionalità aggiuntive senza dover uscire ed eseguire nuovamente un'altra procedura di installazione.

Quando un prodotto usa il programma di installazione, un utente può scegliere in fase di installazione quali funzionalità o applicazioni installare e quali annunciare. Quindi, se durante l'esecuzione di un'applicazione l'utente richiede una funzionalità annunciata che non è ancora stata installata, l'applicazione chiama il programma di installazione per eseguire un'installazione a livello di funzionalità JUST-In-Time dei file necessari. Se l'utente attiva un prodotto annunciato che non è ancora stato installato, il sistema operativo chiama il programma di installazione per eseguire un'installazione just-in-time a livello di prodotto.

[L'annuncio](advertisement.md) e l'installazione su richiesta possono anche semplificare la gestione del sistema consentendo agli amministratori di designare le applicazioni come obbligatorie o facoltative per diversi gruppi di utenti. Esistono due tipi di annunci noti come "assegnazione" e "pubblicazione". Se un amministratore assegna un'applicazione a un gruppo, questi utenti possono installare l'applicazione su richiesta. Se, tuttavia, l'amministratore pubblica l'applicazione nel gruppo, non vengono visualizzati punti di ingresso per questi utenti e l'installazione su richiesta viene attivata solo se un'altra applicazione attiva l'applicazione pubblicata.

 

 



