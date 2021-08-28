---
title: Configurazione dell'applicazione
description: L'installazione di un'applicazione per un singolo utente può creare problemi in un ambiente Servizi Desktop remoto multiutente.
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743eff150edf5e9d213759ccef8c786bab98754b8e4dc2b968929ba3ad2d6709
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099591"
---
# <a name="application-setup"></a>Configurazione dell'applicazione

La procedura di installazione automatica per molte applicazioni esistenti presuppone che l'applicazione venga installata per un singolo utente. In un ambiente multiutente Servizi Desktop remoto, questo presupposto può creare i problemi seguenti:

-   Se la procedura di installazione aggiorna il Registro di sistema e l'ambiente desktop per un solo utente, altri utenti devono reinstallare l'intero pacchetto oppure un amministratore deve copiare manualmente le informazioni dal Registro di sistema e dal desktop di un utente agli altri utenti.
-   Con alcune procedure di installazione, è possibile personalizzare l'applicazione in fase di installazione escludendo le funzionalità. Se il programma di installazione iniziale esclude parte dell'applicazione, altri utenti devono reinstallare l'applicazione per ottenere le funzionalità escluse.

Per evitare questi problemi, le procedure di installazione devono usare le linee guida seguenti quando si installa un'applicazione in un server Host sessione Desktop remoto (Host sessione Desktop remoto):

-   Installare le applicazioni nell'ambiente utente predefinito comune a tutti gli utenti. Prima di installare l'applicazione, eseguire il comando change **user /install** della console e al termine dell'installazione eseguire il comando **change user /execute** console. Usare uno script Servizi Desktop remoto compatibilità per l'installazione.
-   Supportare la personalizzazione specifica dell'utente tramite l'uso di profili utente. A tale scopo, creare un formato [di file modello amministrativo in](/previous-versions/windows/desktop/Policy/administrative-template-file-format) modo che un amministratore possa configurare il Registro di sistema per indicare le funzionalità disponibili per ogni utente. Quindi, in fase di esecuzione, l'applicazione può abilitare o disabilitare le funzionalità a seconda delle impostazioni nelle impostazioni del Registro di sistema dell'utente corrente. L'applicazione può archiviare la configurazione per utente nell'hive del Registro di sistema **HKEY CURRENT USER** e consentire a ogni utente di configurare l'applicazione in base alle proprie preferenze.

 

 